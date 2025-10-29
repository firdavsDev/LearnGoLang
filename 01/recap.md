# 🧭 1-BOSQICH: RECAP (Go Fundamentals — Thinking the Go Way)

---

### 🪄 1. Go’ning falsafasi — “Kamroq sehr, ko‘proq nazorat”

Python → qulay, lekin sekin (dinamik, interpretatsiya qilinadi).
Go → soddaligi orqali kuchli (statik, kompilyatsiya qilinadi, bitta binar fayl).

**Yodda tutish kerak:**

> Go — bu “tejamkorlik” tili. Har bir narsa aniq, o‘qiladigan, lekin juda tez.

---

### 🔹 2. Muhit va birinchi dastur

```bash
go mod init hello
go run main.go
go build
```

```go
package main
import "fmt"
func main() {
    fmt.Println("Salom, Golang!")
}
```

**Farqi:** Python’da `main.py`, Go’da esa `package main` va `func main()` bo‘lmasa, dasturni ishga tushira olmaysiz.

---

### 🔹 3. O‘zgaruvchilar va turlar

```go
var age int = 25
name := "Tohir"
fmt.Printf("%T\n", name) // string
```

**Farq:** `:=` faqat funksiya ichida ishlaydi.
Go’da barcha turlar **aniq** (statik): `int`, `float64`, `bool`, `string`.

---

### 🔹 4. Slice va Map

```go
nums := []int{1, 2, 3}
users := map[string]int{"Ali": 21, "Laylo": 23}
nums = append(nums, 4)
fmt.Println(users["Ali"])
```

**Farqi:** Slice — dinamik array, Map — dict, lekin har ikkalasi **type-safe**.

---

### 🔹 5. Struct va Method

```go
type User struct {
    Name string
    Age  int
}

func (u User) SayHello() {
    fmt.Println("Salom,", u.Name)
}
```

**Farqi:** Klasslar yo‘q, faqat `struct + method`.
Go’da `(u *User)` pointer receiver bilan qiymatni o‘zgartiradi.

---

### 🔹 6. Funksiyalar

```go
func add(a, b int) int { return a + b }

func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, fmt.Errorf("0 ga bo‘lish mumkin emas")
    }
    return a / b, nil
}
```

**Farqi:** Go’da funksiya bir nechta qiymat qaytara oladi — masalan `(result, error)`.

---

### 🔹 7. Error handling

Go’da `try/except` yo‘q.
Har bir funksiya o‘z xatosini **oddiy qiymat sifatida** qaytaradi:

```go
result, err := divide(10, 0)
if err != nil {
    fmt.Println("Xato:", err)
}
```

**Falsafa:** “Xatoni yashirma — uni boshqar.”

---

### 🔹 8. Package va module

```go
go mod init myapp
import "myapp/greet"
```

```go
package greet
func Hello(name string) { fmt.Println("Salom,", name) }
```

**Qoida:**

* `package main` → dasturning boshlanish nuqtasi.
* Katta harf bilan boshlangan funksiya — `public`.
* `init()` → avtomatik ishga tushadi.

---

### 🔹 9. Fayl, JSON va HTTP

**Fayl:**

```go
data, _ := os.ReadFile("data.txt")
fmt.Println(string(data))
```

**JSON:**

```go
jsonData, _ := json.Marshal(user)
json.Unmarshal(jsonData, &user)
```

**HTTP:**

```go
http.HandleFunc("/hello", func(w http.ResponseWriter, r *http.Request) {
    fmt.Fprint(w, "Salom, Go dan!")
})
http.ListenAndServe(":8080", nil)
```

**Farqi:** Django serveri 20 MB, Go serveri 2 MB binar fayl — va 10 baravar tez.

---

### 🔹 10. `if`, `switch`, `for`

```go
if n := 10; n > 5 {
    fmt.Println("Katta")
}

switch day {
case "shanba": fmt.Println("Dam olish")
default: fmt.Println("Ish kuni")
}

for i := 0; i < 5; i++ {
    fmt.Println(i)
}
```

**Go’da while yo‘q**, chunki `for` hammasini qoplaydi.

---

### 🔹 11. Yakuniy loyiha — CLI File Stats Analyzer

Siz yozgan dastur quyidagi bilimlarni birlashtiradi:

* `os.Args` (CLI argumentlar)
* `bufio.Scanner` (fayldan o‘qish)
* `strings.Fields` (so‘z ajratish)
* `if/switch/for`
* `error handling`
* `defer` (resursni tozalash)

---

## 📊 1-bosqich natijasi:

Endi siz:
✅ Go’ni o‘rnatish,
✅ kompilyatsiya qilish,
✅ struct va method yozish,
✅ funksiyalar bilan ishlash,
✅ CLI tool yaratish,
✅ error handling va fayl o‘qish,
✅ JSON va HTTP bilan ishlashni bilasiz.

