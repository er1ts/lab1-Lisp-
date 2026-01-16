<p align="center"><b>МОНУ НТУУ КПІ ім. Ігоря Сікорського ФПМ СПІСКС</b></p>
<p align="center">
<b>Звіт з лабораторної роботи 1</b><br/>
"Обробка списків з використанням базових функцій" <br/>
дисципліни "Вступ до функціонального програмування"
</p>
<p align="right"><b>Студент</b>: Скібчик Арсен група КВ-21</p>
<p align="right"><b>Рік</b>: 2026</p>

## Загальне завдання
Створіть список з п'яти елементів
### Вимоги до списку:
- використати **LIST**, **SET**, **CONS**;
- заборонено використовувати **SETQ** для проміжних значень;
- загальна кількість елементів (разом з підсписками) — **до 10–12**;
- список має містити:
  - хоча б один символ;
  - хоча б одне число;
  - хоча б один непорожній підсписок;
  - хоча б один порожній підсписок.
  ### Необхідно:
1. Отримати голову списку.
2. Отримати хвіст списку.
3. Отримати третій елемент списку.
4. Отримати останній елемент списку.
5. Використати предикати **ATOM** та **LISTP** (2–3 приклади).
6. Використати інші предикати.
7. Об'єднати список з одним із його підсписків за допомогою **APPEND**.
## Завдання 1
```lisp
CL-USER> (defvar lab-list nil)
LAB-LIST
CL-USER> (setq lab-list (list 'alpha 10 (cons 'beta (list 20)) nil 'gamma))
(ALPHA 10 (BETA 20) NIL GAMMA)
CL-USER> 
;; Пункт 1: 
CL-USER> (car lab-list)
ALPHA
;; Пункт 2: 
CL-USER> (cdr lab-list)
(10 (BETA 20) NIL GAMMA)
;; Пункт 3: 
CL-USER> (third lab-list)
(BETA 20)
;; Пункт 4: 
CL-USER> (last lab-list)
(GAMMA)
;; Пункт 5: 
CL-USER> (atom (car lab-list))
T
CL-USER> (atom (third lab-list))
NIL
CL-USER> (listp (third lab-list))
T
CL-USER> (listp (car lab-list))
NIL
;; Пункт 6: Інші предикати
CL-USER> (numberp (second lab-list))
T
CL-USER> (null (fourth lab-list))
T
CL-USER> (symbolp (car lab-list))
T
;; Пункт 7:
CL-USER> (append lab-list (third lab-list))
(ALPHA 10 (BETA 20) NIL GAMMA BETA 20)
```
## Варіант 17
<p align="center"> <img src="lab-1-variant.png" width="500"> </p>

### Виконання завдання:
```lisp
CL-USER> (setq var-list (list 'A (list 'B) 'C (list 'B 1)))
(A (B) C (B 1))
```
