# Mobile Answer Sheet Scanner

แอปพลิเคชัน Flutter สำหรับตรวจกระดาษคำตอบด้วยกล้องมือถือ พร้อมระบบจัดการคะแนนและรายงานผลอัตโนมัติ

## 🎯 คุณสมบัติหลัก

### 📸 การสแกนและตรวจกระดาษคำตอบ
- ใช้กล้องมือถือสแกนกระดาษคำตอบ
- ระบบตรวจจับและประมวลผลคำตอบอัตโนมัติ
- รองรับกระดาษคำตอบหลายรูปแบบ
- แสดงผลการตรวจทันที

### 📊 การจัดการข้อมูลคะแนน
- อัปโหลดเฉลยจากไฟล์ Excel (.xlsx, .xls)
- จัดเก็บข้อมูลในฐานข้อมูลภายในเครื่อง (SQLite)
- สรุปคะแนนตามรายชื่อนักเรียน
- คำนวณคะแนนเฉลี่ยอัตโนมัติ
- ส่งออกผลคะแนนเป็นไฟล์ Excel

### 👥 การจัดการนักเรียน
- เพิ่ม/แก้ไข/ลบข้อมูลนักเรียน
- นำเข้ารายชื่อจาก Excel
- ค้นหาและกรองข้อมูล

### 📈 รายงานและสถิติ
- แสดงสถิติคะแนนโดยรวม
- กราฟแสดงการกระจายคะแนน
- รายงานคะแนนรายบุคคล
- เปรียบเทียบคะแนนระหว่างข้อสอบ

## 🛠️ เทคโนโลยีที่ใช้

- **Framework**: Flutter 3.x
- **Language**: Dart
- **Database**: SQLite (sqflite)
- **Excel Processing**: excel, spreadsheet_decoder
- **Camera**: camera, image_picker
- **Image Processing**: opencv_dart / ml_kit
- **State Management**: Provider / Riverpod / Bloc
- **UI Components**: Material Design 3

## 📁 โครงสร้างโปรเจ็กต์

```
lib/
├── main.dart                 # Entry point
├── models/                   # Data models
│   ├── student.dart
│   ├── answer_sheet.dart
│   ├── exam.dart
│   └── score.dart
├── screens/                  # UI screens
│   ├── home_screen.dart
│   ├── scan_screen.dart
│   ├── student_list_screen.dart
│   ├── score_summary_screen.dart
│   └── settings_screen.dart
├── widgets/                  # Reusable widgets
│   ├── student_card.dart
│   ├── score_chart.dart
│   └── excel_picker.dart
├── services/                 # Business logic
│   ├── database_service.dart
│   ├── excel_service.dart
│   ├── scanner_service.dart
│   └── scoring_service.dart
├── utils/                    # Utilities
│   ├── constants.dart
│   └── helpers.dart
└── providers/                # State management
    ├── student_provider.dart
    └── exam_provider.dart
```

## 🚀 การติดตั้งและใช้งาน

### ความต้องการของระบบ
- Flutter SDK 3.0 ขึ้นไป
- Dart SDK 3.0 ขึ้นไป
- Android Studio / VS Code
- Android 6.0+ หรือ iOS 11.0+

### ขั้นตอนการติดตั้ง

1. Clone repository
```bash
git clone https://github.com/takatb/mobile-answer-sheet-scanner.git
cd mobile-answer-sheet-scanner
```

2. ติดตั้ง dependencies
```bash
flutter pub get
```

3. รันแอปพลิเคชัน
```bash
flutter run
```

### การใช้งานเบื้องต้น

1. **เพิ่มข้อมูลนักเรียน**: นำเข้ารายชื่อจาก Excel หรือเพิ่มด้วยตนเอง
2. **อัปโหลดเฉลย**: เลือกไฟล์ Excel ที่มีเฉลยข้อสอบ
3. **สแกนกระดาษคำตอบ**: ใช้กล้องถ่ายภาพกระดาษคำตอบ
4. **ตรวจและบันทึก**: ระบบจะตรวจและบันทึกคะแนนอัตโนมัติ
5. **ดูรายงาน**: ตรวจสอบคะแนนและสถิติต่างๆ

## 📋 รูปแบบไฟล์ Excel

### ไฟล์เฉลย (Answer Key)
```
| Question | Answer |
|----------|--------|
| 1        | A      |
| 2        | B      |
| 3        | C      |
```

### ไฟล์รายชื่อนักเรียน
```
| StudentID | Name           | Class |
|-----------|----------------|-------|
| 001       | สมชาย ใจดี     | ม.1/1 |
| 002       | สมหญิง รักเรียน | ม.1/1 |
```

## 🎨 ฟีเจอร์ที่กำลังพัฒนา

- [ ] รองรับกระดาษคำตอบหลายประเภท (OMR)
- [ ] ระบบ Cloud Sync
- [ ] ส่งผลคะแนนทาง Email
- [ ] รายงานแบบ PDF
- [ ] Dark mode
- [ ] Multi-language support
- [ ] การวิเคราะห์ข้อสอบ (Item Analysis)

## 🤝 การมีส่วนร่วม

ยินดีรับการมีส่วนร่วมจากทุกคน! กรุณา:

1. Fork โปรเจ็กต์
2. สร้าง Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit การเปลี่ยนแปลง (`git commit -m 'Add some AmazingFeature'`)
4. Push ไปยัง Branch (`git push origin feature/AmazingFeature`)
5. เปิด Pull Request

## 📄 License

โปรเจ็กต์นี้อยู่ภายใต้ MIT License - ดูรายละเอียดในไฟล์ [LICENSE](LICENSE)

## 👨‍💻 ผู้พัฒนา

- **takatb** - [GitHub](https://github.com/takatb)

## 📞 ติดต่อ

หากมีคำถามหรือข้อเสนอแนะ กรุณาเปิด Issue หรือติดต่อผ่าน GitHub

## 🙏 ขอบคุณ

- Flutter Team
- ผู้พัฒนา packages ต่างๆ ที่ใช้ในโปรเจ็กต์
- ชุมชน Flutter Thailand

---

**หมายเหตุ**: โปรเจ็กต์นี้พัฒนาขึ้นเพื่อการศึกษาและช่วยเหลืองานด้านการศึกษา
