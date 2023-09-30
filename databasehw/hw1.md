
# 1.  postgres
1. install
	![[Pasted image 20231001010424.png]]
	![[Pasted image 20231001015927.png]]
1. CREATE USER
![[Pasted image 20230930161434.png]]
1. CREATE DATABASE
![[Pasted image 20230930161423.png]]
1. CREATE TABLE
![[Pasted image 20230930161412.png]]
1. SHOW DATABASES
![[Pasted image 20230930161515.png]]
1. SHOW TABLES
![[Pasted image 20230930161336.png]]
1. SHOW COLUMNS
	![[Pasted image 20230930161607.png]]
1. DESCRIBE
	![[Pasted image 20230930161349.png]]

# 2. main characteristics of database approach 
   1. DBMS儲存特定資料庫的描述，稱爲meta-data
   2. meta-data允許DBMS在不同資料庫軟體裏都能動
   3. 允許使用者並行檢索和更新資料庫。
   5. 允許資料與程式保持獨立，讓使用者可以更改資料已結構而不用更改DBMS
   6. DBMS確保每個transaction 正確執行或中止
   7. 復原系統把每個已完成的Transaction的作用記錄在資料庫中
   8. OPTP允需每秒執行很多併發transactions
   9. 支援多種資料視圖
   10. 資料抽象，讓使用者不需要接觸實際資料儲存細節
   11.  資料庫可以根據使用者權限控制對資料的存取
# 3. define terms
   1. data model: 
   描述資料庫結構、操作這些結構的操作以及資料庫應遵守的某些約束的一組概念，提供實現資料抽象的手段。提供與許多使用者使用資料的方式接近的概念。
   2. database schema：
   資料庫的敘述，包含資料結構種類與限制
# 4. 
   ## 1. three schema architecture:
   1. Internal schema
      *  描述物理儲存架構和存取路徑
   2. Conceptual schema
      * 敘述使用者定義的資料架構與資料限制
   3. External schemas
      * 通常爲data model
      * 敘述部分使用者有興趣的資料，隱藏其他資料
   ## 2.  
   * logical data independence: change the conceptual schema without having to change the external schemas
   * physical data independence: change the internal schema without having to change the conceptual schema.
# 5. 
| | Entity 1 | Cardinality Ratio | Entity 2 |
|-|-|-|-|
|1.| Student |one-to-many|Book|
|2.| Student |many-to-one|Advisor|
|3.| ClassRoom | many-to-many |Wall|
|4.| Student| many-to-many |Course|
|5.| Car| one-to-one |Engine|
1. a student have many book, a book have one owner.
1. a student have one advisor, a advisor have many student.
1. a classroom have many wall, a wall can be two classroom wall.
1. a student have many course, a course have many student.
1. a car have one engine, a engine have only car.
# 6.
## a.
student(<u>Student ID No.</u> , name,  address, ID No. ,cellphone, class, Department/Graduate Institute, suspension)
Suspension(<u>No.</u> , student ID No. , Term of suspension, signature, signed by parent, date of resumption, date of application, application)
## b.
![[Pasted image 20231001015727.png]]