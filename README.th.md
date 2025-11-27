<div align="center">
<img height=150 src="https://github.com/naaive/orange/blob/master/src-tauri/icons/icon.png" />
</div>
<p align="center">
<span>ภาษาไทย</span> | <a href="README.md">English</a> | <a href="README_cn.md">中文</a>
</p>
<p align="center"><span>แอปพลิเคชันเดสก์ท็อปข้ามแพลตฟอร์ม สำหรับค้นหาไฟล์ในเครื่อง</span></p>

<div align="center">

[![Download Counts](https://img.shields.io/github/downloads/naaive/orange/total?style=flat)](https://github.com/naaive/orange/releases)
[![Stars Count](https://img.shields.io/github/stars/naaive/orange?style=flat)](https://github.com/naaive/orange/stargazers)
[![Forks Count](https://img.shields.io/github/forks/naaive/orange.svg?style=flat)](https://github.com/naaive/orange/network/members)
[![LICENSE](https://img.shields.io/badge/license-gpl-green?style=flat)](https://github.com/naaive/orange/blob/master/LICENSE)

[![Windows Support](https://img.shields.io/badge/Windows-0078D6?style=flat&logo=windows&logoColor=white)](https://github.com/naaive/orange/releases)
[![MACOS Support](https://img.shields.io/badge/MACOS-adb8c5?style=flat&logo=macos&logoColor=white)](https://github.com/naaive/orange/releases)
[![Linux Support](https://img.shields.io/badge/linux-1793D1?style=flat&logo=linux&logoColor=white)](https://github.com/naaive/orange/releases)
</div>

## Orange คืออะไร?

![Demo](https://s1.ax1x.com/2022/05/20/OO4e61.gif)

Orange เป็นแอปพลิเคชันเดสก์ท็อปสำหรับ **ค้นหาไฟล์** ในเครื่อง

## ✨คุณสมบัติ

- ตอบสนองการค้นหาได้รวดเร็ว
- ใช้หน่วยความจำและซีพียูต่ำ
- ใช้งานง่าย มาพร้อมการตัดคำและเติมคำอัตโนมัติ
- สามารถติดตามความเปลี่ยนแปลงไฟล์แบบเรียลไทม์
- แพคเกจติดตั้งขนาดเล็ก น้ำหนักเบา
- หน้าตา UI เรียบง่ายและสวยงาม

## ธีมที่รองรับ 
- มีให้เลือก 3 ธีม (เปลี่ยนได้ที่เมนู Settings ในโปรแกรม)
    1. Default (เข้ม)
    2. Light Purple (ม่วงสว่าง)
    3. Light Blue (ฟ้าสว่าง)

## วิธีการ Build, ติดตั้ง และรันทดสอบ

### 1. เตรียมความพร้อม
- ติดตั้ง Node.js, Yarn, Rust, Tauri CLI (ดู https://tauri.app/v1/guides/getting-started/prerequisites/)

### 2. Clone และ Build
```bash
# Clone repo และเข้าโฟลเดอร์โปรเจกต์
 git clone https://github.com/phuphadang-alpha/orange.git
 cd orange
 git checkout translate-th  # สาขาไทย

# ติดตั้ง dependency
 yarn

# Build frontend (React)
 yarn build

# Build Tauri (desktop app)
 yarn tauri build
```

### 3. Run (สำหรับ development)
```bash
yarn tauri dev
```

### 4. สร้าง Installer หรือ Portable สำหรับ Windows/Mac/Linux
- ดูเอกสาร https://tauri.app/v1/guides/distribution/ ในการสร้าง installer แบบ *.exe, *.dmg หรือ portable executable ใช้งานได้ (นำไปใส่แฟลชไดรฟ์ได้ด้วย)

## การทดสอบ (Testing)

### ทดสอบฟีเจอร์หลักบนเครื่องจริง
1. ค้นหาไฟล์, ค้นหาโฟลเดอร์ (พิมพ์ชื่อไฟล์แบบต่างๆ)
2. ทดสอบเปลี่ยนธีมและภาษาได้ทันที (Settings)
3. ลองเพิ่ม/ลบไฟล์ ในโฟลเดอร์ที่ถูก monitor โปรแกรมควรอัปเดตอัตโนมัติ
4. ทดสอบ Exclude Paths (ตั้งค่าการละเว้นโฟลเดอร์)
5. ตรวจสอบ memory/cpu ว่าต่ำ

### ทดสอบฝั่ง backend (Rust) ด้วย unit test
```bash
cd src-tauri
cargo test
```

## หมายเหตุ
- ถ้านำไปพัฒนา portable เพิ่มเติมให้ config/database อยู่ในโฟลเดอร์เดียวกับไฟล์ .exe จะสามารถเปิดโดยไม่ผูกกับ user folder ได้
- ไม่เหมาะกับ Codespaces/X11 remote
- ถ้า merge/sync กับ main ให้ดึง branch translate-th ก่อน

## ขอบคุณ
- Tauri https://tauri.studio
- Notify https://github.com/notify-rs/notify
- React https://github.com/facebook/react
- Tantivy https://github.com/quickwit-oss/tantivy
- Kv https://github.com/zshipko/rust-kv

## LICENSE

[GPL](https://github.com/naaive/orange/blob/master/LICENSE)