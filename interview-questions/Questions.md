# обязательно подготовить к собеседованию
- массивы и слайсы (почитать исходники)
- строки (почитать исходники)
- пакет sync(мьютексы, вейт группы, атомик)
- каналы (почитать исходники)
- планировщик (кстати, многозадачность с версии 1.14 стала полностью preemptive)
- базы данных 
    - acid(4 уровня изоляции)
    - cap теорема
    - инедксы(b-tree, hash-map, кластерный, некластерный)
    - запрос на having и group by
- алгоритмы и структуры данных
    - осноные структуры данных
    - специфика типа skip list, bloom filter и т.д. очень стоит почитать про вероятностные структуры данных
    - основные задачи с литкода: https://github.com/frankegoesdown/preparing_yandex_interview/
    - https://tproger.ru/translations/14-templates-to-answer-interview-questions/ основные паттерны здесь разбираются
- дизайн
    - https://tianpan.co/notes/2016-02-13-crack-the-system-design-interview
    - https://github.com/donnemartin/system-design-primer#real-world-architectures

# собесодования лидов 
- что такое kpi сотрудника, как его посчитать, как посчитать свой
- мотивация
- системы оценки персонала
- agile, scrum, kanban

# common screening questions

- Что такое сложность алгоритма?
- Что такое хэштаблицы?
- Что такое B tree?
- Чем having отличается от where?
- Есть ли в го эксепшны?
- Какими либами для баз в го пользовался?
- Какими СУБД пользовался?
- Как определить рейсы в коде?
- Что такое мьютекс и как он используется?
- Как убить процесс в линуксе?
- Что такое -9 и потом какие бывают еще сигналы?
- Как убить процесс по имени?
- Как посчитать количество строк в файле?
- Как посчитать количество уникальных строк в файле?
- Как попасть на конкретный коммит?
- Как откатить ветку к конкретному коммиту?
- Как перенести коммит из одной ветки в другую?
- Какие я помню HTTP методы?
- Из чего состоит HTTP запрос, если просто сделать его дамп в текст?
- Как разделяются заголовки и тело запроса в тексте?
- Есть ли в го сеты из питона?
- А если очень хочется, как сделать сет?
- Суть REST-подхода при построении API.
- бинарные протоколы обмена данными?
- Что такое GraphQL?

- Какие структуры данных ты знаешь?
- Как устроена хеш-мапа? Время поиска? Время вставки? Коллизии и способ из разрешения? Применение?
- Как устроен массив? Время поиска? Время вставки? Применение?
- Как устроен стек? Время доступа? Время вставки? Применение?
- Как устроен связный список? Время поиска? Время вставки? Применение?
- Как устроено бинарное дерево? Время поиска? Время вставки? Применение?
- Какие алгоритмы сортировки ты знаешь? Сложность?
- Что такое mutex?
- Что такое deadlock?
- Стек и куча
- За что отвечает параметр GOMAXPROCS?

# coding tasks

```
package main

// Что выведет?
func main() {

	names := []string{"john", "dave", "mike"}

	for i := range names {
		go func() {
			println(names[i])
		}()
	}
}
```

```
package main

// В чем ошибка?
func main() {

	ch := make(chan int)

	go func() {
		for i := 0; i < 10; i++ {
			ch <- i
		}
	}()

	for n := range ch {
		println(n)
	}
}
```

```
package main

// Что выведет?
func main() {
	s := "mañana"
	println(len(s))
}
```

```
package main

import "fmt"

// Что выведет?
func main() {
	numbers := [10]int{0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
	s := numbers[1:5:10]
	fmt.Printf("%v %d %d", s, len(s), cap(s))
}
```

```
import (
    "fmt"
)
 
func main() {
    a := [5]int{76, 77, 78, 79, 80}
    var b []int = a[1:4]
    fmt.Println(b)
}
```

```

package main

type customError struct {
	msg string
}

func (e *customError) Error() string {
	return e.msg
}

func test() *customError {
	{
		// do something
	}
	return nil
}

func main() {
	var err error
	err = test()
	if err != nil {
		println("error")
		return
	}
	println("ok")
}
```

```
package main

import (
	"fmt"
)

func add(arr []int, v int) {
	arr[0] = 100
	arr = append(arr, v)
}

// Что выведет?
func main() {
	arr := make([]int, 2)
	fmt.Printf("%v %p\n", arr, &arr)
	add(arr, 10)
	fmt.Printf("%v %p\n", arr, &arr)
}
```

```
package main
 
import (
    "fmt"
)
 
 
func test() (x int) {
    defer func() {
        x++
    }()
    x = 1
    return
}
 
 
func anotherTest() int {
    var x int
    defer func() {
        x++
    }()
    x = 1
    return x
}
 
 
func main() {
    fmt.Println(test())
    fmt.Println(anotherTest())
}
```

```
package main
 
import (
    "fmt"
    "os"
)
 
func Foo() error {
    var err *os.PathError = nil
    return err
}
 
func main() {
    err := Foo()
    fmt.Println(err)
    fmt.Println(err == nil)
}
```

```
package main
 
import (
  "fmt"
)
 
func main() {
  var s = []string{"1", "2", "3"}
  modifySlice(s)
  fmt.Println(s)
}
 
func modifySlice(i []string) {
  i[0] = "3"
  i = append(i, "4")
  i[1] = "5"
  i = append(i, "6")
}
```
