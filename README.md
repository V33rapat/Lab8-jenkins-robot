# Lab 8: Docker & Jenkins Pipeline with Robot Framework

Repository นี้เป็นส่วนหนึ่งของแบบฝึกปฏิบัติที่ 8  
รายวิชา Software Engineering  
มีวัตถุประสงค์เพื่อฝึกการใช้งาน Docker, Jenkins และ Robot Framework  
ตั้งแต่การ build image, run container ไปจนถึงการสร้าง Jenkins Pipeline อย่างง่าย

## วัตถุประสงค์ของแบบฝึกปฏิบัติ

- เข้าใจการใช้งาน Docker image และ Docker container
- สามารถเขียน Dockerfile เพื่อ build image ได้
- เข้าใจการทำงานของ Jenkins และการตั้งค่า Jenkins ผ่าน Docker
- สร้าง Pipeline อย่างง่ายเพื่อรัน Robot Framework test
- ฝึกการจัดการ Source code บน GitHub ร่วมกับ Jenkins

## โครงสร้างของ Repository

```text
.
├── Jenkinsfile
├── README.md
└── tests/
    └── Lab8.robot
```

### รายละเอียดไฟล์
- Jenkinsfile
  - ใช้กำหนดขั้นตอนการทำงานของ Jenkins Pipeline เช่น การแสดงผลข้อความ หรือการรัน test

- tests/Lab8.robot
  - ไฟล์ทดสอบที่เขียนด้วย Robot Framework สำหรับใช้ทดสอบระบบในขั้นตอน UAT

### เครื่องมือที่ใช้

- Docker Desktop
- Jenkins (รันบน Docker Container)
- Robot Framework
- GitHub

### ขั้นตอนการทำงานโดยสรุป

- Build Docker image สำหรับ Jenkins และ Environment ที่รองรับ Robot Framework
- Run Jenkins container และผูกพอร์ตที่ 8080
- เข้าใช้งาน Jenkins ผ่าน Browser ที่ http://localhost:8080
- สร้าง Jenkins Pipeline และเชื่อมต่อกับ GitHub Repository
- ใช้ Jenkinsfile เพื่อ execute ขั้นตอนการทำงาน
- รัน Robot Framework test จากโฟลเดอร์ tests/

### หมายเหตุ

- Repository นี้จัดทำขึ้นเพื่อการศึกษาและการเรียนรู้เท่านั้น
