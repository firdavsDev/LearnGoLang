
# 🧩 1-BOSQICH AMALIY VAZIFALAR

---

### 🅰️ **A-daraja (asosiy)** — “Matn statistikasi CLI tool”ni yaxshilash

**Maqsad:** Siz yozgan `Go File Stats Analyzer` dasturini rivojlantiring.

#### 🔧 Vazifa:

1. Foydalanuvchi CLI orqali quyidagi flaglardan birini berishi mumkin bo‘lsin:

   * `--lines` → faqat satrlar sonini chiqarish
   * `--words` → faqat so‘zlar sonini chiqarish
   * `--longest` → faqat eng uzun so‘zni chiqarish
2. Hech narsa berilmasa — hamma statistikani chiqarish.

#### 💡 Maslahatlar:

* `flag` paketini ishlating.
* `switch` yordamida flag’ni tahlil qiling.
* `fmt.Errorf()` bilan custom error yozing:

  ```go
  return fmt.Errorf("noto‘g‘ri flag: %s", flag)
  ```

---

### 🅱️ **B-daraja (o‘rta)** — “Mini To-do List CLI”

**Maqsad:** `slice`, `for`, `switch`, `os`, `bufio` bilimlarini qo‘llash.

#### 🔧 Vazifa:

CLI’da quyidagi buyruqlarni qo‘llab-quvvatlaydigan to-do dastur yozing:

```bash
go run main.go add "kitob o‘qish"
go run main.go list
go run main.go remove 2
```

#### 🔍 Talablar:

* Ma’lumotlar `tasks.txt` faylida saqlansin.
* `add` yangi qator qo‘shadi.
* `list` tartib raqamlari bilan chiqarsin.
* `remove <index>` berilgan tartibdagi satrni o‘chiradi.
* Faylni o‘qish/yozishda `bufio` va `strings` paketlaridan foydalaning.
* CLI argumentlar uchun `os.Args` yoki `flag` ishlating.

---

### 🅾️ **C-daraja (qiyinroq)** — “Go File Merger”

**Maqsad:** Go’da fayllar bilan murakkabroq amaliyot.

#### 🔧 Vazifa:

1. Foydalanuvchi quyidagicha buyruq beradi:

   ```bash
   go run main.go file1.txt file2.txt output.txt
   ```
2. Dastur:

   * `file1.txt` va `file2.txt` ni o‘qib,
   * ularni birlashtirib (`\n` bilan ajratib),
   * `output.txt` faylga yozadi.
3. Har bir fayldagi **satrlar sonini** hisoblab, yakunda konsolga chiqaradi:

   ```
   file1.txt -> 12 satr
   file2.txt -> 9 satr
   Umumiy -> 21 satr
   ```

#### 💡 Qo‘shimcha:

* Error handling (`if err != nil`) har bir fayl uchun alohida bo‘lsin.
* `defer file.Close()` har bir ochilgan faylga alohida ishlasin.
* Eng yaxshi yechim — funksiya modulli tarzda bo‘lishi:

  ```go
  func countLines(filename string) (int, error)
  func mergeFiles(file1, file2, output string) error
  ```

---

## 🧠 Yakuniy maqsad:

Bu uchta vazifa sizni:

* `os`, `bufio`, `strings`, `flag` bilan mustahkam qiladi;
* `if`, `switch`, `for` va `error handling`ni real kontekstda ishlatishga majbur qiladi;
* va 2-bosqichga (Functions, Panic, Modular Design) **tayyor** holga keltiradi.

