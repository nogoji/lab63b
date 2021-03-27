# การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)

## วัตถุประสงค์
1. เพื่อใช้ไมโครคอนโทรลเลอร์เป็นตัวปล่อยสัญญาณไวไฟ
2. ศึกษาโปรแกรมที่ทำให้ไมโครคอนโทรลเลอร์เป็นตัวปล่อยสัญญาณไวไฟ

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรลเลอร์ ชนิด ESP-01
2. สาย USB to Serial
3. คอมพิวเตอร์ตั้งโต๊ะหรือแลปท็อป

## ศึกษาข้อมูลเบื้องต้น
สามารถศึกษาการเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ไดที่ [คลิปการทดลองนี้](https://www.youtube.com/watch?v=T26DVHePlTs) [โค้ดการทดลองนี้](https://github.com/choompol-boonmee/lab63b/blob/master/examples/06_Wifi-AP-Web-Server/src/main.cpp) และสามารถศึกษาเพิ่มเติมได้ที่เว็บไซต์ [platformio.org](http://platformio.org/)

## วิธีการทำการทดลอง
1. ต่อไมโครคอนโทรลเลอร์เข้ากับ USB to Serial
2. ไปยังไฟล์ของโปรแกรมนี้ แล้วศึกษาโปรแกรมได้ที่ [โค้ดการทดลองนี้](https://github.com/choompol-boonmee/lab63b/blob/master/examples/06_Wifi-AP-Web-Server/src/main.cpp)
    * ส่วนแรก กำหนดชื่อไวไฟและรหัสผ่านไวไฟ ต่อมาใส่ IP Adress ของไมโครคอนโทรลเลอร์ ชนิด ESP-01 นี้
    
    ![2021-03-27 (22)](https://user-images.githubusercontent.com/80879891/112718039-17272200-8f23-11eb-9c9c-76a4ce705f75.png)

    * ส่วนที่สอง เป็นการเตรียมเว็บเซอร์เวอร์ไว้หนึ่งตัว โดยสร้างแอคเซสพอยต์ด้วย *soft.AP* และใส่ IP ที่เรากำหนดไว้
    
    ![2021-03-27 (21)](https://user-images.githubusercontent.com/80879891/112718174-cbc14380-8f23-11eb-9f0d-fa114302607a.png)

3. รันคำสั่ง *pio run -t upload* เพื่ออัปโหลดโปรแกรมไปยังไมโครคอนโทรลเลอร์
4. ขณะที่กำลังอัปโหลด กดปุ่มรันตามด้วยปุ่มรีเซ็ต
5. รันคำสั่ง *pio device monitor* 
6. ทดสอบนำโทรศัพท์หรือคอมพิวเตอร์มาค้นหาไวไฟจากไมโครคอนโทรลเลอร์ ว่ามีอยู่หรือไม่

## การบันทึกผลการทดลอง
ได้ไวไฟที่สามารถเชื่อมต่อได้จากไมโครคอนโทรลเลอร์ โดยใช้รหัสผ่านไวไฟที่กำหนดไว้
![2021-03-27 (23)_LI](https://user-images.githubusercontent.com/80879891/112718467-c8c75280-8f25-11eb-8d4c-d891aabec0f7.jpg)

## อภิปรายผลการทดลอง
การทดลองนี้เป็นประโยชน์ต่อไมโครคอนโทรลเลอร์อย่างมาก เพราะสามารถทำให้มีไวไฟได้ในตัวเอง และสามารถปล่อยสัญญาณให้อุปกรณ์อื่นได้อีกด้วย
และยังเป็นประโยชน์ต่อผู้ใช้งานทำให้เมื่อไม่มีไวไฟใช้ สามารถใช้ไวไฟได้จากไมโครคอนโทรลเลอร์ได้

## คำถามหลังการทดลอง
ถ้าไม่รู้ IP Adress ของไมโครคอนโทรลเลอร์ ก็ไม่สามารถสร้างไวไฟใช่หรือไม่