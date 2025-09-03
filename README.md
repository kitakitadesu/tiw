# Function ที่คิดว่าจำเป็นต่อการสอบ

[Made by ออกัส FRAB12 aka @kitakitadesu on Discord](https://hi.bocchichan.moe/)

![Kita chan](kita.jpg)

`len()`: คืนค่าความยาว (จำนวนไอเท็ม) ของอ็อบเจกต์ เช่น ความยาวของ str หรือ list

`max()`: คืนค่าไอเท็มที่ใหญ่ที่สุดในลิสต์ หรือค่าที่ใหญ่ที่สุดเมื่อมีอาร์กิวเมนต์ตั้งแต่สองตัวขึ้นไป

`min()`: คืนค่าไอเท็มที่เล็กที่สุดในลิสต์ หรือค่าที่เล็กที่สุดเมื่อมีอาร์กิวเมนต์ตั้งแต่สองตัวขึ้นไป

`int()`: คืนค่าอ็อบเจกต์ที่เป็นจำนวนเต็ม (integer) จากตัวเลขหรือสตริง

`float()`: คืนค่าตัวเลขทศนิยม (floating point) จากตัวเลขหรือสตริง

`type()`: คืนค่าชนิด (type) ของอ็อบเจกต์ใดๆ

`str()`: สร้างสตริงเปล่าขึ้นมาใหม่

`upper()`: คืนค่าสตริงที่เป็นตัวพิมพ์ใหญ่ทั้งหมด

`lower()`: คืนค่าสตริงที่เป็นตัวพิมพ์เล็กทั้งหมด

`list()`: สร้างลิสต์ว่าง (list) ขึ้นมาใหม่

`sum()`: คืนค่าผลรวมของไอเท็มทั้งหมดในลิสต์ (ใช้ได้กับลิสต์ของตัวเลข)

`append()`: เพิ่มไอเท็ม 1 ตัวเข้าไป ต่อท้าย ลิสต์

`extend()`: ขยาย ลิสต์โดยการนำไอเท็มทั้งหมดจากลิสต์อื่นมาต่อท้าย

`insert()`: แทรก ไอเท็ม ณ ตำแหน่ง (index) ที่กำหนด

`remove()`: ลบ ไอเท็มตัวแรกที่เจอซึ่งมีค่าตรงกับที่ระบุ

`pop()`: ดึง ไอเท็ม ณ ตำแหน่งที่กำหนดออกจากลิสต์ (และคืนค่าไอเท็มนั้นออกมา)

`index()`: คืนค่า ตำแหน่ง (index) ของไอเท็มที่ระบุ

`count()`: นับ และคืนค่าจำนวนครั้งที่ไอเท็มนั้นปรากฏในลิสต์

`sort()`: จัดเรียง ไอเท็มในลิสต์จากน้อยไปมาก

`sort(reverse=True)`: จัดเรียง ไอเท็มในลิสต์จากมากไปน้อย

`reverse()`: สลับลำดับ ไอเท็มในลิสต์ (จากหน้าไปหลังเป็นหลังไปหน้า)


# ตัวอย่างการใช้

```python
numbers = [10, 5, 80, 25]


print(len(numbers))   # ผลลัพธ์: 4 (เพราะมี 4 อย่างใน list ชื่อว่า numbers)
print(max(numbers))   # ผลลัพธ์: 80 (ค่าที่มากที่สุด)
print(min(numbers))   # ผลลัพธ์: 5 (ค่าที่น้อยที่สุด)
```

```python
num_str = "123"
float_str = "99.5"


# แปลง string เป็น integer (เลขจำนวนเต็ม)
real_num = int(num_str)
print(real_num * 2)   # ผลลัพธ์: 246


# แปลง string เป็น float (เลขทศนิยม)
real_float = float(float_str)
print(real_float + 0.5) # ผลลัพธ์: 100.0
```

```python
print(type(100))        # ผลลัพธ์: <class 'int'>
print(type("สวัสดี"))    # ผลลัพธ์: <class 'str'>
print(type("สวัสดี") == str)    # True
print(type([1, 2, 3]))  # ผลลัพธ์: <class 'list'>
```

```python
year = 2025
# เราไม่สามารถนำ "ข้อความ" + 2025 ได้โดยตรง ต้องแปลงเลขเป็นข้อความก่อน
text = "ปีนี้คือปี " + str(year)
print(text)           # ผลลัพธ์: ปีนี้คือปี 2025
```

```python
kitachan = "Bocchi The Rock!"


print(kitachan.upper())  # ผลลัพธ์: 'BOCCHI THE ROCK!'
print(kitachan.lower())  # ผลลัพธ์: 'bocchi the rock!'
```python
words = ["Bocchi", "The", "Rock!"]
separator = "_"


# ใช้ "_" เป็นตัวคั่นระหว่างคำ
sentence = separator.join(words)
print(sentence)         # ผลลัพธ์: 'Bocchi_The_Rock!'
```

```python
# list() สร้างลิสต์ว่าง
my_list = list()
print("ลิสต์ว่าง:", my_list)      # ผลลัพธ์: ลิสต์ว่าง: []


# เริ่มต้นด้วยลิสต์ผลไม้
fruits = ["apple", "banana", "cherry"]

print("ลิสต์ตัวที่ 0 คือ :", fruits[0]) # ผลลัพธ์: ลิสต์ตัวที่ 0 คือ : apple
print("ลิสต์ตัวที่ 1 คือ :", fruits[1]) # ผลลัพธ์: ลิสต์ตัวที่ 1 คือ : banana
print("ลิสต์ตัวที่ 2 คือ :", fruits[2]) # ผลลัพธ์: ลิสต์ตัวที่ 2 คือ : cherry


# append() เพิ่ม 1 ไอเท็มต่อท้าย
fruits.append("orange")
print("หลัง append:", fruits)     # ผลลัพธ์: หลัง append: ['apple', 'banana', 'cherry', 'orange']


# extend() เพิ่มทุกไอเท็มจากอีกลิสต์มาต่อท้าย
more_fruits = ["mango", "grape"]
fruits.extend(more_fruits)
print("หลัง extend:", fruits)     # ผลลัพธ์: หลัง extend: ['apple', 'banana', 'cherry', 'orange', 'mango', 'grape']


# insert() แทรกไอเท็มที่ตำแหน่ง (index) 1
fruits.insert(1, "blueberry")
print("หลัง insert:", fruits)    # ผลลัพธ์: หลัง insert: ['apple', 'blueberry', 'banana', 'cherry', 'orange', 'mango', 'grape']


# remove() ลบไอเท็มโดยระบุค่าของมัน
fruits.remove("banana")
print("หลัง remove:", fruits)     # ผลลัพธ์: หลัง remove: ['apple', 'blueberry', 'cherry', 'orange', 'mango', 'grape']


# pop() ดึงไอเท็มออกจากตำแหน่งที่ระบุ (index 2 คือ 'cherry') แล้วคืนค่านั้นออกมา
removed_fruit = fruits.pop(2)
print("ไอเท็มที่ถูกดึงออก:", removed_fruit) # ผลลัพธ์: ไอเท็มที่ถูกดึงออก: cherry
print("ลิสต์ล่าสุด:", fruits)               # ผลลัพธ์: ลิสต์ล่าสุด: ['apple', 'blueberry', 'orange', 'mango', 'grape']


# เพิ่ม 'apple' เข้าไปอีก 1 เพื่อทดสอบการนับ
fruits.append("apple")
print("ลิสต์ปัจจุบัน:", fruits)    # ผลลัพธ์: ลิสต์ปัจจุบัน: ['apple', 'blueberry', 'orange', 'mango', 'grape', 'apple']


# index() หาตำแหน่งของ 'orange'
pos = fruits.index("orange")
print("ตำแหน่งของ orange:", pos)  # ผลลัพธ์: ตำแหน่งของ orange: 2 (list นับเริ่มต้นจาก 0)
# 0 คือ apple
# 1 คือ blueberry
# 2 คือ orange
# ถัดไปเรื่อยๆๆ


# count() นับจำนวน 'apple' ในลิสต์
num_apples = fruits.count("apple")
print("มี apple ทั้งหมด:", num_apples) # ผลลัพธ์: มี apple ทั้งหมด: 2
```

```python
numbers = [45, 22, 100, 15, 8]


# sort() จัดเรียงจากน้อยไปมาก
numbers.sort()
print("หลัง sort:", numbers)      # ผลลัพธ์: หลัง sort: [8, 15, 22, 45, 100]


# sort(reverse=True) จัดเรียงจากมากไปน้อย
numbers.sort(reverse=True)
print("หลัง sort reverse:", numbers) # ผลลัพธ์: หลัง sort reverse: [100, 45, 22, 15, 8]


# reverse() สลับลำดับจากหน้าไปหลัง
numbers.reverse()
print("หลัง reverse:", numbers)   # ผลลัพธ์: หลัง reverse: [8, 15, 22, 45, 100]


# sum() หาผลรวมของตัวเลขทั้งหมดในลิสต์
total = sum(numbers)
print("ผลรวม:", total)           # ผลลัพธ์: ผลรวม: 190
```
