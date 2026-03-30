# 🎓 Internship Management System (Project)
ระบบจัดการการฝึกงานสำหรับนิสิต

---

## ภาพรวมโปรเจกต์ (Project Overview)
ระบบเว็บแอปพลิเคชันสำหรับอำนวยความสะดวกในการยื่นคำขอฝึกงาน การอนุมัติโดยอาจารย์ที่ปรึกษา และการบันทึกประวัตินิเทศงาน

### ฟีเจอร์หลัก:
* **นิสิต:** ยื่นคำขอฝึกงาน, เลือกบริษัท, ตรวจสอบสถานะการอนุมัติ
* **อาจารย์:** อนุมัติ/ไม่อนุมัติคำขอ, บันทึกการนิเทศงานและให้คะแนน
* **เจ้าหน้าที่:** จัดการข้อมูลบริษัท, ออกใบส่งตัว, ดูรายงานภาพรวม

---

## โครงสร้างฐานข้อมูล (Database Structure)
เราใช้ **MySQL** ในการจัดการข้อมูล โดยมีตารางหลักดังนี้:

* **Users:** `student`, `teacher`, `faculty_staff`
* **Master Data:** `company`, `status_master`, `course_showcase`
* **Transactions:** `internships_request`, `status_log`, `supervision_record`

> 📄 **รายละเอียดเชิงลึก:** สามารถดูได้ที่ไฟล์ [Data_Dictionary_v1.pdf](./database/Data_Dictionary_v1.pdf) ในโฟลเดอร์ `/database`

---

## สถานะระบบ (Status Codes)
เพื่อให้การเขียน PHP if-else ตรงกัน ให้ใช้รหัสสถานะตามนี้:
* `1` : **Pending** (รับเรื่อง/รออนุมัติ)
* `2` : **Approved** (อาจารย์อนุมัติ)
* `3` : **Issued** (ออกใบส่งตัวแล้ว)
* `4` : **Completed** (ฝึกงานเสร็จสิ้น)
* `9` : **Rejected** (ยกเลิก/ไม่ผ่าน)

---

## วิธีการติดตั้งและรันโปรเจกต์ (Setup Guide)
1. **Database:** - เปิด XAMPP > MySQL Admin (phpMyAdmin) หรือ DBeaver
   - สร้าง Database ชื่อ `internships`
   - Import ไฟล์ `/database/internships.sql` เข้าไป
2. **Source Code:**
   - นำโฟลเดอร์โปรเจกต์ไปวางที่ `C:/xampp/htdocs/`
3. **Configuration:**
   - เช็คไฟล์ `connect.php` ว่า Username/Password ของ MySQL ตรงกับเครื่องตัวเองไหม
4. **Access:**
   - เปิดเบราว์เซอร์ไปที่ `http://localhost/internships_system/login.php`

---

## 🤝 การแบ่งงานในทีม (Team Collaboration)
* **Database & Backend Logic:** [ไอโกะ ณัฏฐณิชา พลาธรณ์ 67101010619]
* **Frontend & UI Design:** [ฟีฟ่า ธฤษณัช ภานุกาญจน์ 67101010128,
ใบเตย สุนัดดา แสงแก้ว 67101010132]
* **System Logic & Integration:** [เนเน่ ชลธิชา คุณเพิ่มศิริ 67101010617, โต๋ ภูรินท์ กูลมนุญ 67101010641]
* **Flowchart internship และรูปแล่มโครงงาน** [พลอย ณิชาภัทร จันทร์เอี่ยม 67101010620]

---

**⚠️ หมายเหตุ:** หากมีการแก้ไขโครงสร้างตาราง รบกวนแจ้ง DBA พื่ออัปเดตไฟล์ SQL กลางทุกครั้ง!
