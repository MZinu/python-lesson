## Файл удирдах

Файлтай харьцах нь аливаа вэб програмын чухал хэсэг юм.
Python нь файл үүсгэх, унших, шинэчлэх, устгах хэд хэдэн функцтэй.
Python дахь файлуудтай ажиллах гол функц нь open() функц юм.
Open () функц нь хоёр параметрийг авдаг (файлын нэр, горим).

**Файлыг нээх дөрвөн өөр арга (горим) байдаг:**
```
"r" - Унших - Үндсэн утга. Файлыг унших боломжгүй бол алдаа гардаг
"a" - Нэмэх - Хавсралтад зориулж файлыг нээнэ, хэрэв байхгүй бол файлыг үүсгэдэг
"w" - Бичих - Бичих файлыг нээнэ, байхгүй бол файлыг үүсгэнэ
"x" - Үүсгэх - Тодорхойлогдсон файлыг үүсгэдэг, хэрэв файл байгаа бол алдааг буцаадаг
```
**Мөн файлыг хоёртын болон текст горимоор ажиллуулах эсэхийг тодорхойлж болно**
```
"t" - Текст - Үндсэн утга. Текст горим
"b" - Хоёртын - хоёртын горим (жишээ нь зураг)
```
### Синтакс - бичигдэх хэлбэр
Файлыг уншихаар нээхийн тулд файлын нэрийг зааж өгөхөд хангалттай.
```
f = open("demofile.txt") # анхны утга нь "r" байдаг
f = open("demofile.txt", "rt") # бичвэр файл уншихаар заасан
```

### Жишээ
1. demo.txt файлд дараах бичвэрийг оруул
```
Hello! Welcome to demo.txt
This file is for testing purposes.
Good Luck!
```
2. app.py файлд дараах кодыг бичнэ
```
f = open("demofile.txt", "r")
print(f.read())   #print(f.read(5)) эхний 5 тэмдэгт
```

3.
```
f = open("demofile.txt", "r")
print(f.readline())
print(f.readline())
```
4.
```
f = open("demofile.txt", "r")
for x in f:
  print(x)
```
5.
```
f = open("demofile.txt", "r")
print(f.readline())
f.close()
```

6. 
```
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()
f = open("demofile2.txt", "r")
print(f.read())
```
7. 
```
import os
os.remove("demofile.txt")
```
8.
```
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")
```
9.
```
import os
os.rmdir("myfolder")
```
