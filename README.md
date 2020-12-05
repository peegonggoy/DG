# Data Governance
## What is Data Governance ?
**_Data Governance_** แปลเป็นไทยว่า การธรรมาภิบาลข้อมูล ซึ่งหมายถึง การกำหนดสิทธิ หน้าที่ และความรับผิดชอบของผู้มีส่วนได้ส่วนเสียในการ**บริหารจัดการข้อมูลทุกขั้นตอน** เพื่อให้ได้มาและการนำไปใช้ข้อมูลของหน่วยงานภาครัฐ **ถูกต้อง ครบถ้วน เป็นปัจจุบัน รักษาความเป็นส่วนบุคคล** และ**เชื่อมโยงกันได้อย่างมีประสิทธิภาพ** และ**มั่นคงปลอดภัย** โดยใช้ **ข้อมูลเป็นหลักในการขับเคลื่อนประเทศ** 

## Why Data Governance ?
เพราะ Data ที่เกิดขึ้นในองค์กร มีความกระจัดกระจาย ทำให้ไม่สามารถเข้าถึงชุดข้อมูลเดียวกันได้ แม้จะอยู่ในองค์กรเดียวกัน ส่งผลให้องค์กรไม่สามารถนำ Data นั้นไปใช้ประโยชน์ได้อย่างเต็มที่ การมี Data Governance ก่อให้เกิดกฎระเบียบในการบริหารจัดการข้อมูลที่ชัดเจนขึ้น และยังช่วยลดความเสี่ยงในการเกิดข้อมูลซ้ำซ้อน ข้อมูลไม่มีคุณภาพ และการหวงแหนข้อมูลได้อีกด้วย

ผลลัพธ์ที่ได้จากการทำ Data Governance ไม่ใช่แค่เอกสารที่เป็นกฎระเบียบขององค์กรเท่านั้น แต่ต้องมีการปรับเปลี่ยนระบบ Infrastructure ใหม่เสียด้วย เพราะการเข้าถึงข้อมูล จะต้องโปร่งใส และมีการกำหนดสิทธิในการเข้าถึงข้อมูลอย่างชัดเจน ดังนั้นในท้ายที่สุดของการผลักดันโครงการ Data Governance จะเป็นการปรับเปลี่ยนวิธีการทำงานขององค์กรทั้งหมด เพื่อรองรับการทำงานแบบ Data-Driven Business นั่นเอง

[![jZoChy.png](https://sv1.picz.in.th/images/2020/12/05/jZoChy.png)](https://www.picz.in.th/image/jZoChy)

## ประเด็นในการจัดการ Data Governance มีอะไรบ้าง ?
การจัดการ Data Governance จะครอบคุมในกรอบใหญ่ๆดังต่อไปนี้ Data Quality, Data Assurances, Security, Policy โดยอธิบายเพิ่มเติมได้ดังนี้

* **Lineage** จะต้องอธิบายที่ไปที่มาของข้อมูล เพราะในโลกความเป็นจริง เวลาเราทำ Data Lake ข้อมูลมันอาจจะมีความหลากหลาย ทั้งแบบ Structured, Un-Structured, Semi-Structured สิ่งที่ต้องระบุกำกับในแต่ละข้อมูลคือ ถ้าหากเป็น Data Set อาจจะบอกว่า มาจาก Data Set อื่นอีกที นำมาบางส่วนหรือสำเนามาทั้งหมด ถ้าหากเป็น Database อาจจะต้องระบุว่า Column นี้ถูก Join หรือคำนวณมาจาก Field ไหนบ้าง เพื่อเป็นประโยชน์สำหรับการ tracking และต่อนักวิเคราะห์ข้อมูลด้วย เพราะในโลกของ Data Lake Big Data นักวิเคราะห์อาจเป็น Data Science
* **Audit** จะต้องทราบเหตุการณ์ต่างๆที่เกิดขึ้นกับข้อมูล โดยบันทึก Log ของกิจกรรมที่จำเป็น เช่น กิจกรรมประเภท CRUD (Create, Rename, Update, Delete)  รวมไปจนถึงใครนำเข้าข้อมูลเพิ่ม เวลาไหน เมื่อไหร่ หากระบบมี API เรียกจากภายนอกก็ต้องบันทึกเหตุการณ์การเชื่อมต่อนั้นๆลง Log ไว้ด้วย เพื่อประโยชน์ทางด้านงานตรวจสอบนั้นเอง
* **Security** ในด้านความปลอดภัย ครอบคุมถึงการกำหนดนโยบายการเข้าถึงข้อมูลหรือ Data Set ทั้งในระดับ User, Roles, Group โดยอนุญาติสิทธิ์ตามจำเป็น เช่น เข้าถึงเพื่อดูได้อย่างเดียว หรือดูและแก้ไขส่วนไหนได้บ้าง ในด้าน Security นี้จะครอบคุมถึงความปลอดภัยของการจัดเก็บข้อมูลด้วย เช่น การเข้ารหัสข้อมูลบางชนิดเป็นต้น
* **Data Quality** หากข้อมูลไม่สมบูรณ์ ไม่ถูกต้อง การนำไปวิเคราะห์ใช้งานก็ผิด ส่งผลต่อความน่าเชื่อถือของระบบ ในส่วนนี้จึงให้ความสำคัญกับการจัดความถูกต้องของข้อมูล กระบวนการที่เกี่ยวข้องเช่น Data Cleansing, Data Preparation เพื่อลด missing value, duplication value, invalid format ปัจจุบันมีเครื่องมือที่เข้ามาช่วยดูในเรื่องนี้มากมาย โดยส่วนใหญ่จะเป็น Function เกี่ยวกับ Data Profiling เพราะจะมีรูปแบบการตรวจสอบข้อมูลในแต่ละแบบให้เราเลยว่า ลักษณะของข้อมูลเราเป็นอย่างไร เพื่อแก้ไขได้ง่าย รวดเร็ว และถูกต้อง
* **Compliance** ในส่วนนี้ขึ้นอยู่กับธุรกิจของเราด้วยว่าทำอะไร เช่นหากเป็นธุรกิจด้านการทำธุรกรรมการเงิน ซื้อขายหลักทรัพย์ ก็จะมีฏกหมาย ระเบียบข้อบังคับที่ต้องให้ดำเนินการตาม ในส่วนนี้เราเพียงตรวจสอบให้มั่นใจว่า การควบคุมข้อมูลเป็นไปตาม Compliance ของธุรกิจเราทำอยู่หรือไม่ เช่น ในปัจจุบันมีกฏหมาย GDPR ออกมา เราก็จะต้องตรวจสอบว่า ถ้าข้อมูลเรามีข้อมูลส่วนบุคคลของคนยุโรปเพราะบริษัทเราทำธุรกิจกับประเทศแถบยุโรป เราจะต้องรักษาข้อมูลอย่างไรเพื่อให้สอดคล้องกับ GDPR เป็นต้น
 * **Certification of Data** ควรมีกระบวนการอนุมัติหรือมีการให้ระดับหรือเรทของข้อมูลสำหรับ Data Set หรือ Data Model ที่ถูกตรวจสอบแล้วว่าถูกต้อง หรือการตรวจสอบองค์ประกอบความสมบูรณ์ต่างๆครบตามนโยบายกำหนด เพื่อให้ผู้ใช้งานข้อมูลมีความน่าเชื่อถือกับตัวข้อมูล เช่น ข้อมูลที่อยู่ลูกค้า ข้อมูลยอดขาย เป็นต้น ของประเทศไทยเราก็จะมีชุดข้อมูลที่เรียกว่า High Value Data เป็นต้น
* **Cataloging and Metadata** ควรจะมีส่วนที่รวบรวมข้อมูลในระบบทั้งหมด พร้อมทั้งข้อมูลประกอบคำอธิบายของข้อมูลชุดนั้น เช่น แหล่งที่มา ใครคือเจ้าของข้อมูล ใช้ทำอะไร และอื่นๆตามองค์ประกอบของ Lineage เพื่อเป็นข้อมูลสำหรับ Data Analyst หรือ Data Scientist นำมาใช้

## Data Governance life circle
**1.Data Ownership Discovery<br>**
การระบุแหล่งที่มาของข้อมูลและผู้รับผิดชอบ โดยจะต้องชี้แจงรายละเอียดของการได้มาซึ่งข้อมูล เช่น กรอกข้อมูลในระบบใด มีรูปแบบการเก็บอย่างไร ฝ่ายใดเป็นผู้รับผิดชอบ หรือเป็นเจ้าของข้อมูล เป็นต้น 

**2.Data Policy and Risk Level<br>**
การระบุความเสี่ยงของข้อมูล และ กำหนดระดับความเป็นส่วนตัวของข้อมูล โดยสามารถแบ่งระดับความเสี่ยงเป็นระดับ เช่น ข้อมูลความลับ ข้อมูลสาธารณะ เพื่อใช้เป็นตัวบ่งชี้ในการบริหารข้อมูลด้านความปลอดภัย ซึ่งผู้กำหนดระดับความเสี่ยงของข้อมูลนี้ คือ หน่วยงานผู้รับผิดชอบข้อมูลโดยตรง 

**3.Data Proliferation<br>**
การระบุความเชื่อมโยงของการกำเนิด ใช้งาน และทำลายข้อมูล ในขั้นตอนนี้ จะเป็นการเขียน Flow เพื่อมองหาจุดเชื่อมโยงของข้อมูล เช่น ฝ่ายบัญชี ได้รับข้อมูลมาจากระบบ POS และระบบ ERP ซึ่งผู้รับผิดชอบกรอกข้อมูลใน ERP ประกอบไปด้วยส่วนหน้าร้าน ส่วนคลังสินค้า ส่วนขนส่ง และส่วนงานออกแบบผลิตภัณฑ์ เป็นต้น โดย Flow นี้  สามารถเขียนเป็นกล่องเชื่อมโยงอย่างง่าย โดยไม่จำเป็นต้องวาดเป็น ER-Diagram เพราะวัตถุประสงค์ของ Flow เพราะให้เห็นถึงการเชื่อมโยงข้อมูลกันในเชิงปฏิบัติ ดังนั้น คนที่เขียน Flow นี้ อาจจะไม่ใช่กลุ่มงาน IT แต่อาจเป็น Data Analyst หรือ ผู้มีหน้าที่รับผิดชอบโครงการ Data Governance ทั้งนี้ ผลลัพธ์ที่ได้จากการทำ Data Proliferation คือ การออกแบบโครงสร้างของข้อมูลใหม่ เพื่อให้สามารถนำข้อมูลไปใช้ที่ปลายทางได้อย่างมีประสิทธิภาพมากขึ้น โดยมีส่วนของการเชื่อมโยงข้อมูล (Data Integration), การทำความสะอาดข้อมูล (Data Cleansing) และการออกแบฐานข้อมูลใหม่ (Database Design) มาเกี่ยวข้องด้วย 

**4.Data Dictionary<br>**
การร่างเอกสารเพื่อระบุสถานะ การจัดเก็บข้อมูล ซึ่ง Data Dictionary เป็นพื้นฐานที่ทุกองค์กรควรจะมี เพราะเอกสารฉบับนี้ เป็นเอกสารที่บ่งบอกได้ว่า มีการเก็บข้อมูลอะไรเอาไว้ที่ไหนบ้าง อย่างไรก็ตาม ในแต่ละช่วงเวลา Data Dictionary จะมีการเปลี่ยนแปลงไป เป็นเพราะมีข้อมูลใหม่ๆ เข้ามาในระบบมากขึ้น ดังนั้นหน่วยงานที่มีหน้าที่จัดทำ และ Update เอกสาร Data Dictionary คือ หน่วยงาน IT หรือ Data Admin ทั้งนี้ ปัญหาขององค์กรใหญ่ที่มีการลงระบบมานาน พบว่า ไม่ได้มีการเก็บ Data Dictionary เอาไว้ และเมื่อระบบเป็นระบบใหญ่ ทำให้ยากต่อการสร้าง Data Dictionary ใหม่ อาจจะเป็นเพราะก่อนหน้านี้ Vendor ที่มาลงระบบไว้ ไม่ได้มอบ Data Dictionary ให้ก็เป็นได้ แต่เมื่อต้องดำเนินการในโครงการ Data Governance ก็เลี่ยงไม่ได้ที่จะต้องมี Data Dictionary เพราะจำเป็นจะต้องระบุความรับผิดชอบของข้อมูลนั่นเอง

**5.Data Protection<br>**
การออกแบบช่องทางการป้องกันข้อมูล เป็นงานต่อเนื่องจากขั้นตอนที่ 2 และ 3 โดยในส่วนที่ 5 Data Protection นี้ จะเป็นการออกแบบระบบ ตามหลักความปลอดภัย หรือ Database Security ซึ่งกระบวนการนี้ จำเป็นต้องมีการ Review การออกแบบ Infrastructure ใหม่ทั้งหมด เพื่อรอบรับระดับความเสี่ยงของชุดข้อมูลแต่ละชุด ซึ่งในยุคก่อน จะมีการสร้าง Data Warehouse ที่เดียว และติดตั้งระบบ Security แบบเดียว แต่ในปัจจุบัน เนื่องจากการเข้าถึงข้อมูล ควรมีการบริหารจัดการที่ยืดหยุ่น และเปิดให้เข้าถึงได้ตามสิทธิ์ ทำให้การออกแบบ Data Warehouse ไม่จำเป็นต้องมีแค่ที่เดียวอีกต่อไป 

**6.Data Access and Authorization<br>**
การออกแบบระบบเพื่อให้ผู้ใช้งานสามารถเข้าถึงข้อมูลได้ตามสิทธิ หรือ ขอ Request ข้อมูลได้จากผู้มีอำนาจในการอนุมัติสิทธิ เป็นการเปลี่ยนรูปแบบการทำงาน จากที่เมื่อก่อนการจะขอข้อมูลจะมีหน่วยงาน IT เป็นคนดึงข้อมูลให้ แต่หากมีการออกแบบระบบแบบใหม่ จะสามารถเปิดโอกาสให้ผู้ใช้งานสามารถเลือกใช้ข้อมูลได้ตามระดับของความเสี่ยงของข้อมูล ซึ่งหากข้อมูลมีความลับ หรือเป็นข้อมูลที่จำกัดสิทธิ์ ก็สามารถกรอกรายละเอียดการขอข้อมูลผ่านระบบได้ เพื่อส่งรายงานไปยังผู้อนุมัติได้โดยตรง ซึ่งระบบการขออนุมัตินี้ ทางหน่วยงาน IT จะเป็นผู้รับผิดชอบออกแบบระบบ และดูแลรักษาระบบ ซึ่งการมีระบบนี้ จะทำให้ข้อมูลทั้งหมด มีความโปร่งใส และเป็นแนวทางทางในการแก้ปัญหาการหวงแหนข้อมูลได้เป็นอย่างดี        จะเห็นได้ว่า ทั้ง 6 ข้อนี้ จะมีทั้งส่วนการรับผิดชอบแบ่งออกเป็น ส่วนเจ้าของข้อมูล หน่วยงาน IT และผู้มีความต้องการใช้ข้อมูล ซึ่งการดำเนินโครงการ Data Governance ที่ดี ควรคำนึงถึงการนำไปใช้จริงให้ได้มากที่สุด ไม่ใช่แค่เป็นนโยบายในกระดาษ แต่จะต้องมีการออกแบบ Infrastructure ใหม่เสียงหมด เพื่อรองรับการเข้าถึงข้อมูลได้อย่างโปร่งใส

![DGLC](https://static.wixstatic.com/media/dbb365_41c50c348eb1408c8bb915d9be05a468~mv2.png/v1/fill/w_708,h_315,al_c,q_90,usm_0.66_1.00_0.01/dbb365_41c50c348eb1408c8bb915d9be05a468~mv2.webp)


เรียบเรียงเนื้อหาโดย Bhoomjit Bhoominath 05/12/2563

## Reference
* [https://www.softnix.co.th/2018/09/02/data-governance-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3-%E0%B8%97%E0%B8%B3%E0%B9%84%E0%B8%A1%E0%B8%88%E0%B8%B6%E0%B8%87%E0%B8%AA%E0%B8%B3%E0%B8%84%E0%B8%B1%E0%B8%8D%E0%B8%95/](https://www.softnix.co.th/2018/09/02/data-governance-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3-%E0%B8%97%E0%B8%B3%E0%B9%84%E0%B8%A1%E0%B8%88%E0%B8%B6%E0%B8%87%E0%B8%AA%E0%B8%B3%E0%B8%84%E0%B8%B1%E0%B8%8D%E0%B8%95/)
* [https://www.coraline.co.th/single-post/data-governance](https://www.coraline.co.th/single-post/data-governance)
* [https://www.dga.or.th/th/profile/2108/](https://www.dga.or.th/th/profile/2108/)
