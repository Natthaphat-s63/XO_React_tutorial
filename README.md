# Commit 1 : Initialize react project

สร้าง React โปรเจคโดยใช้ คำสั่ง npx create-react-app xo-project จากนั้นทำการลบไฟล์ที่ไม่จำเป็นและแก้ไขโค้ดที่ต่อไปถึงไฟล์นั้น โดยมี
- App.test.js
- logo.svg
- reportWebVitals.js
- setupTests.js <br>


จากนั้นแก้ไขโค้ดในส่วนของ App.js โดยลบทั้งหมดใน return แล้วใส่แค่ div tag <br>


# Commit 2 : Create Board,Square and Game Components

สร้าง File ชื่อ Board.js, Square.js และ Game.js โดยทั้งสามไฟล์เป็น Components จากนั้นทำการเขียนในไฟล์ Board.js โดยสร้างเป็น Class Component ที่มีชื่อ Board โดยมี Function ชื่อ renderSquare โดยรับ parameter i แล้วทำการ return เป็น Square Component ส่งค่า i เป็น props เป็น value ฉะนั้น Board ทำหน้าที่ส่งสร้าง Square ตามจำนวน i จากนั้น Function render ทำการ return โดยเรียกใช้ renderSquare โดยส่งเลขเป็นเลขตำแหน่งปุ่ม 0-8 ส่วนใน File Square.js เป็น Class Component เหมือนกันโดยมี Function render ทำหน้าที่ return ปุ่มที่มี className เป็น square โดยเเสดงผลข้อความตามค่า value ที่รับมาผ่าน props ส่วน Game.js เรียกใช้ Board สุดท้ายใน App.js ทำการเรียกใช้ Game อีกทีหนึ่ง


# Commit 3 : Edit index.css for beautiful UI

เปลี่ยน Code ใน index.css ให้เป็นไปตามใน Tutorial เพื่อเปลี่ยนรูปแบบแต่ละ Component ให้สวยงามขึ้น


# Commit 4 : Add Constructor and EventListener in Square Component

สร้าง EventListener โดยให้รับเป็น Event การกดคลิกเมาส์ ซึ่งเป็น HTML Attribute ของ Button ก็คือ onClick โดยให้เป็น Function ที่ทำการแสดงข้อความว่า click ใน console ของ Browser จากนั้นสร้าง constructor ของ Square เพื่อให้รับ props ได้ จากนั้นสร้าง state เริ่มต้น โดยให้ค่า value เป็น null

# Commit 5 : Change onClick function to setState for displaying X

เปลี่ยนจาก function onClick จากที่แสดงบน console log เป็นการเปลี่ยน state ของ Square ให้มีค่า value เป็น X แล้วเปลี่ยนข้อความบนปุ่มเป็นค่า state.value นั้น ดังนั้นเวลาที่เรากดปุ่ม จะแสดงค่า X บนช่อง

# Commit 6 : Move stored game state from Square to Board and create handleClick function in Board

ลบ constructor ของ Square แล้วไปสร้าง constructor สำหรับเก็บ state ของตัวเกม XO ไว้ใน Board แทนเพื่อที่จะสามารถเก็บข้อมูลของทั้งตารางได้ เเละ สร้าง handleClick function เพื่อรับค่า index ของช่องที่ถูกกดและเปลี่ยนค่าของช่องนั้นให้เป็น X แล้วเก็บค่า state ของตำแหน่งนั้นๆ