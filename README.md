# GoLang Backend Yo‘li (“From Python to Go Hero”)

### **1-bosqich (1–10 kun): Go Fundamentals — “Thinking the Go Way”**

**Maqsad:** Pythoncha fikrlashdan Gocha fikrlashga o‘tish.

* Go’ni o‘rnatish, `go mod`, `go run`, `go build`
* `package main`, `func main()` — Go dasturining yuragi
* O‘zgaruvchilar, `var`, `:=`, tur tahlili (type inference)
* `if`, `switch`, `for` (Go’da `while` yo‘qligi va sababi)
* `array`, `slice`, `map` bilan ishlash
* `struct` va `method` (Go’dagi mini-klasslar)
* Python’dagi `class` ↔ Go’dagi `struct + method` solishtiruv
* Dars yakuni: CLI tool yozish — “Go File Stats Analyzer”

---

### **2-bosqich (11–20 kun): Functions, Error Handling va Packages**

**Maqsad:** Toza, modular kod yozishni o‘rganish.

* Funksiyalar, return ko‘rsatkichlari, variadic params
* Error handling — `error` turi va `fmt.Errorf()`
* `panic`, `recover` va `defer` — xavfsiz xatolarni boshqarish
* Standart kutubxonalar (`fmt`, `os`, `io`, `strings`, `net/http`)
* Python’dagi `try/except` bilan solishtirish
* Dars yakuni: CLI log parser (fayldan log o‘qib, tahlil qilish)

---

### **3-bosqich (21–30 kun): Concurrency — “Go Routines and Channels”**

**Maqsad:** Go kuchi — parallel ishlovchi dasturlar.

* `goroutine` nima va qachon ishlatish kerak
* `channel` — thread-safe ma’lumot almashinuvi
* `select` va `sync.WaitGroup` bilan boshqarish
* `context` bilan goroutinelarni to‘xtatish
* Python’dagi `asyncio` bilan farqlar
* Dars yakuni: Parallel fayl yuklovchi app (concurrency practice)

---

### **4-bosqich (31–40 kun): Go bilan Web Backend**

**Maqsad:** Django’dagi API logikasini Go’da yaratish.

* `net/http`, `mux`, `gin` bilan API yozish
* JSON bilan ishlash (`encoding/json`)
* Middleware yozish (auth, logging)
* JWT, REST CRUD, PostgreSQL (`database/sql`, `gorm`)
* Docker bilan Go servisini konteynerlash
* Dars yakuni: “Mini Blog API” (auth, CRUD, JWT, PostgreSQL)

---

### **5-bosqich (41–50 kun): Advanced Topics + Microservices**

**Maqsad:** Go servislarni real dunyoda integratsiya qilish.

* `grpc` va protobuf asoslari
* RabbitMQ bilan xabar almashish
* Go va Django o‘rtasida RPC orqali bog‘lanish
* Caching (Redis bilan)
* Profiling va Performance (pprof, benchmark)
* Dars yakuni: Django bilan birga ishlaydigan “Report Generator microservice”

---

### **6-bosqich (51–60 kun): Yakuniy 5 Loyihalar**

**Maqsad:** Sizni “Go backend dev” darajasiga olib chiqish.

1. **Core Project #1:** Go File Analyzer CLI (struct + goroutine)
2. **Core Project #2:** Log Parser & Notifier (error monitoring tool)
3. **Web API #1:** Mini Blog REST API (JWT + CRUD + Postgres)
4. **Web API #2:** Todo App (gin + gorm + Docker + Redis)
5. **Microservice Project:** Django ↔ Go gRPC Report Service

