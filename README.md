```go
import (
    "fmt"
    "strings"
)

type Me struct {
    Name      string
    Age       int8
    Languages []string
}

func About(Name string, Age int8, Languages []string) Me {
    return Me{Name: Name, Age: Age, Languages: Languages}
}

func (m *Me) Profile() string {
    return fmt.Sprintf("Name: %s\nAge: %d\nLanguages: %s", m.Name, m.Age, strings.Join(m.Languages, " / "))
}

func main() {
    me := About("João Pedro", 22, []string{"Go", "Python", "NodeJs"})
    fmt.Println(me.Profile())
}
