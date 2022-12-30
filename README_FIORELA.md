## Pruebas Unitarias

### JEST

Es común en JavaScript que el código se ejecute de forma asíncrona. Cuando tiene un código que se ejecuta de forma asíncrona, Jest necesita saber cuándo se ha completado el código que está probando, antes de poder pasar a otra prueba. Jest tiene varias formas de manejar esto.

TEST STUDENTS

```
require("dotenv").config();
const express = require("express");
const mysql = require("mysql2");
const StudentController = require("../src/interfaces/controllers/student.controller");
const studentDb = new StudentController();


describe("connection", () => {
  beforeAll(async () => {
    await mysql.createPool({
      host: process.env.HOST,
      user: process.env.USER,
      database: process.env.DATABASE,
      password: process.env.PASSWORD,
    });
  });

  test("Get Course By ID", async () => {
    const id = 1;
    const course = await studentDb.findByIdCourse(id)
    console.log(course);
    expect(course).not.toBe(null);
  });

  test("Get All student", async () => {
    const student = await studentDb.getAll();
    console.log(student);
    expect(student).not.toBe(null);
  });

  test("Get All", async () => {
    const id = 1;
    const course = await studentDb.findByIdCourse(id)
    console.log(course);
    expect(course).not.toBe(null);
  });
});
```

TEST COURSES

```



```
