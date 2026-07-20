# Week-04-Lab-1
### 4.  บันทึกผลการทดลอง 

#### 4.1 จาก `idf.py monitor` 

```
W (256) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (269) main_task: Started on CPU0
I (279) main_task: Calling app_main()
I (279) LAB1_RGB_TIMING: RGB LED Timing System Started.
I (279) LAB1_RGB_TIMING: Phase R: ON
I (2779) LAB1_RGB_TIMING: Phase R: OFF
I (2779) LAB1_RGB_TIMING: Phase G: ON
I (5279) LAB1_RGB_TIMING: Phase G: OFF
I (5279) LAB1_RGB_TIMING: Phase B: ON
I (7779) LAB1_RGB_TIMING: Phase B: OFF
I (7779) LAB1_RGB_TIMING: Entering Rest Phase... Waiting for residual charge to dissipate.
-----------------------------------------------------------
I (10779) LAB1_RGB_TIMING: Phase R: ON
I (13279) LAB1_RGB_TIMING: Phase R: OFF
I (13279) LAB1_RGB_TIMING: Phase G: ON
I (15779) LAB1_RGB_TIMING: Phase G: OFF
I (15779) LAB1_RGB_TIMING: Phase B: ON
I (18279) LAB1_RGB_TIMING: Phase B: OFF
I (18279) LAB1_RGB_TIMING: Entering Rest Phase... Waiting for residual charge to dissipate.

```

#### 4.2 จากการสังเกตุ LED 
ไฟติดแบบสลับสี สีแรกที่เริ่มคือสีแดง สีต่อมาคือสีเขียว และสุดท้ายคือสีแดง จะมีการพักก่อนเริ่มวนซ้ำอีกรอบประมาณ2-3วิครับ





# Week-04-Lab-2
✍️ กิจกรรมวิเคราะห์ผลและการบ้านท้ายใบงาน (Data Science & Engineering Reflection)
การพล็อตพฤติกรรมทางกายภาพ (Transient Response Curve):

ให้นักศึกษาก๊อปปี้ข้อมูลตัวเลขชุดคู่อันดับ No, ADC Raw จาก Serial Monitor ทั้งหมดนำไปวางในโปรแกรม Microsoft Excel หรือ Google Sheets จากนั้นทำการพล็อตกราฟเส้น (Line Chart) โดยให้แกน X เป็นลำดับแซมเปิ้ล (1-20) และแกน Y เป็นค่าดิบของ ADC และแนบรูปกราฟลงในเล่มรายงาน
## สีแดง
<img width="685" height="442" alt="image" src="https://github.com/user-attachments/assets/e2bd251e-9900-4f20-8fa2-ea8335d25eb7" />

## สีเขียว
<img width="696" height="437" alt="image" src="https://github.com/user-attachments/assets/e8ce2ede-e2aa-4235-921a-64982cf550e6" />

## สีน้ำเงิน
<img width="716" height="442" alt="image" src="https://github.com/user-attachments/assets/719b0d48-b83f-4fb1-94c0-59f62ae8b151" />

คำถามนำเพื่อการวิเคราะห์เชิงระบบ (Critical Thinking):

จากกราฟที่พล๊อตออกมา นักศึกษาสังเกตเห็นแนวโน้มตัวเลขของค่า ADC ตั้งแต่แซมเปิ้ลที่ 1 ไต่ระดับลงมาหรือขึ้นไปจนถึงแซมเปิ้ลที่ 20 อย่างไร?

สัญญาณไฟฟ้าเข้าสู่ความนิ่ง (Settling) ที่แซมเปิ้ลใด หรือใช้เวลากี่มิลลิวินาที?

ความลาดเอียงของเส้นกราฟที่เกิดขึ้นในช่วงแรกของการสลับสถานะไฟนี้ เป็นหลักฐานเชิงประจักษ์สะท้อนข้อจำกัดคุณสมบัติทางกายภาพใดของรอยต่อ PN บน LED ภาครับ และโครงสร้างตัวเก็บประจุสุ่มสัญญาณภายในไมโครคอนโทรลเลอร์?

หากในใบงานถัดไปเราต้องการ "หาค่าเฉลี่ยของระดับแรงดันสะท้อนที่แท้จริง" โดยไม่ให้เฟสสัญญาณที่กำลังเปลี่ยนแปลง (Transient State) นี้ไปดึงค่าสถิติให้เพี้ยน นักศึกษาคิดว่าเราควรเลือกแซมเปิ้ลช่วงใดมาคำนวณ หรือควรเขียนโปรแกรมหน่วงเวลาหลบเลี่ยงอาการ Settling นี้อย่างไร?



### Week-04-Lab-3
