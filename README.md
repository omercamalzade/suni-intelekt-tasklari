# suni-intelekt-tasklari#
#Task3a#


# 1
def salam():
    print("Salam, Dünya!")

# 2
def kub_hesabla(n):
    return n ** 3

# 3
def birlesdir(soz1, soz2):
    return soz1 + " " + soz2

# 4
def cap_et(lst):
    for item in lst:
        print(item)

# 5
def toplam(*args):
    return sum(args)

# 6
def ortalama(*args):
    if len(args) == 0:
        return "Rəqəm yoxdur"
    return sum(args) / len(args)

# 7
def adlar_rəqəmlər(**kwargs):
    for ad, reqem in kwargs.items():
        print(f"ad: {ad}, rəqəm: {reqem}")

# 8
def tip_yoxla(dəyər):
    if isinstance(dəyər, str):
        print("mətn")
    elif isinstance(dəyər, (int, float)):
        print("rəqəm")
    else:
        print("başqa")

# 9
def yas_kateqoriya():
    yas = int(input("Yaşınızı daxil edin: "))
    if yas < 18:
        print("Gənc")
    else:
        print("Yetkin")

# 10
def soz_uzunluq():
    soz = input("Bir söz daxil edin: ")
    print(len(soz))

# TASK 3B #    



x = 5
if x > 0:
    print("müsbət")
elif x < 0:
    print("mənfi")
else:
    print("sıfır")

# 2
n = 4
if n % 2 == 0:
    print("cüt")
else:
    print("tək")

# 3
a, b, c = 10, 5, 20
print(max(a, b, c))

# 4
day = 3
günlər = {
    1: "Bazar ertəsi", 2: "Çərşənbə axşamı", 3: "Çərşənbə",
    4: "Cümə axşamı", 5: "Cümə", 6: "Şənbə", 7: "Bazar"
}
print(günlər.get(day, "Yanlış gün"))

# 5
temp = 15
if temp < 0:
    print("soyuq")
elif temp <= 20:
    print("normal")
else:
    print("isti")

# 6
password = "sifre123"
if len(password) < 8:
    print("qısa")
elif len(password) <= 12:
    print("orta")
else:
    print("uzun")

# 7
x = 15
if x % 3 == 0 and x % 5 == 0:
    print("3 və 5")
elif x % 3 == 0:
    print("3")
elif x % 5 == 0:
    print("5")
else:
    print("heç biri")

# 8
for i in range(0, 21, 2):
    print(i)

# 9
s = "Bağda ərik var idi …"
for ch in s:
    print(ch)

# 10
for i in range(1, 11):
    if i == 3:
        continue
    print(i)

# 11
i = 1
while True:
    if i % 5 == 0:
        print(i)
        break
    i += 1

# 12
lst = [1, 3, 5, 7, 9]
for i in range(len(lst)):
    if lst[i] == 5:
        print(i)
        break
# TASK 4A #  

    # 1
def hesabla():
    try:
        a = float(input("Birinci rəqəm: "))
        b = float(input("İkinci rəqəm: "))
        əməl = input("Əməliyyat (+, -, *, /): ")

        if əməl == "+":
            print(a + b)
        elif əməl == "-":
            print(a - b)
        elif əməl == "*":
            print(a * b)
        elif əməl == "/":
            print(a / b)
        else:
            print("Yanlış əməliyyat!")
    except ZeroDivisionError:
        print("0-a bölmək olmaz!")
    except ValueError:
        print("Yalnız rəqəm daxil edin!")
    except Exception as e:
        print("Xəta baş verdi:", e)
    finally:
        print("Hesablama bitdi")

# 2
print([i for i in range(1, 51) if i % 11 == 0])

# 3
sözlər = ["kitab", "qələm", "defter", "silgi"]
print([s[0] for s in sözlər])

# 4
şəhərlər = ["Bakı", "Gəncə", "Sumqayıt"]
kodlar = [12, 22, 18]
print(dict(zip(şəhərlər, kodlar)))

# 5
km_to_mil = lambda km: km * 0.621371
for km in [1, 5, 10, 20, 50]:
    print(km_to_mil(km))

# 6
qiymətlər = [100, 200, 300, 400]
yeni_qiymətlər = list(map(lambda x: x * 1.18, qiymətlər))
print(yeni_qiymətlər)

# 7
list1 = [3, 7, 12]
list2 = [2, 4, 6]
cem = list(map(lambda x, y: (x*2) + (y*2), list1, list2))
print(cem)

# 8
from functools import reduce
qiymətlər = [150, 80, 220, 45]
ən_kiçik = reduce(lambda x, y: x if x < y else y, qiymətlər)
print(ən_kiçik)
