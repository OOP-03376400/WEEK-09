# WEEK-09
# Generics

Generic ช่วยให้ลดภาระในการเขียนโปรแกรม ในลักษณะที่มีอัลกอริทึมเดียวกันแต่ใช้ data type ต่างกัน
ตัวอย่าง Stack

<p align="center">
<img src="https://github.com/OOP-2559/WEEK-09/blob/master/imgs/Picture1.png?raw=true" width="300">
</p>


ในการเขียนโปรแกรม เรามักจะเจอสถานการณ์ที่ใช้อัลกอริทึมเดียวกันกับตัวแปรหลายๆ ชนิด

เนื่องจาก  C# เป็นภาษาแบบ strong type ซึ่งจะมีความเข้มงวดในการใช้งานตัวแปรชนิดต่างๆ พิจารณาจากภาพต่อไปนี้
<p align = "center">
<img src="https://github.com/OOP-2559/WEEK-09/blob/master/imgs/Picture3.png" width="300">
<img src="https://github.com/OOP-2559/WEEK-09/blob/master/imgs/Picture4.png" width="300">

</p>

เราอาจแก้ไขโดยการสร้างคลาสขึ้นมา เพื่อใช้เฉพาะกับชนิดข้อมูลต่างๆ เช่น
###Class myIntStack
``` cs
class myIntStack
{
    int stackPointer = 0;
    int[] StackArray;
    public void Push(int x)
    {
       // push data into stack
    }

    public int Pop()
    {
       // pop data into stack
       return Pop_int_data;
    }
    ....
}

```
###Class myFloatStack
``` cs
class myFloatStack
{
    int stackPointer = 0;
    float[] StackArray;
    public void Push(float x)
    {
       // push data into stack
    }

    public float Pop()
    {
       // pop data into stack
       return Pop_float_data;  //
    }
    ....
}

```
__ที่จริงแค่ คัดลอก และ เปลี่ยน ก็ได้แล้ว ปัญหาคืออะไร???__

* ถ้าเปลี่ยนไม่ครบทุกตำแหน่ง?
* ถ้ามีชนิดอื่นๆ เพิ่มเข้ามาอีก เช่น double, long, string, ฯลฯ
* แล้วมันกินที่ใน source code เพิ่ม?
* แล้วถ้าพบว่า algorithm ผิด ต้องตามไปแก้กี่ที่?
* แล้วไม่คิดจะลองหาวิธีที่ดีกว่าหรือ?






