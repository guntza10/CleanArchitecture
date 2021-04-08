# CleanArchitecture

-> เป็น Architecture ที่เราจะแยกออกเป็น 3 Layer หลัก

- Domain => จะเก็บพวก class model ต่างๆ เช่น Entity(class model schema table),model ทั่วไป, enum, interface
- Infrastructure => เป็นที่เอาไว้ config ต่างๆ เกี่ยวกับ external resource เช่น config เกี่ยวกับการเชื่อมต่อ database, การ map class model entity กับ table schema
- Application => เป็นตัวจัดการเกี่ยวกับ business logic

## ข้อดี

- เราแยกจัดการ presentation logic,business logic,data access ออกจากกันทำให้ reuse code ได้ง่าย code มีความอ่านง่าย
- Dependent of framework => การที่เราแยก layer ออกจากกันชัดเจนทำให้เราสามารถเอาไปใช้กับ Project อื่นๆได้ง่าย เนื่องจาก layer แต่ละส่วนก็จัดการแต่ละหน้าที่ของใครของมันแยกจากกัน (สามารถ Migrate ไปใช้ได้ง่าย)
- Testable => สามารถ test ได้ง่าย
