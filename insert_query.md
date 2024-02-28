## Insert query to add new data for all the tables

```bash
INSERT INTO student (id, first_name, last_name, grade, dob, age)
VALUES (501, 'John', 'Doe', '12', '2005-05-15', 17),
       (502, 'Jane', 'Smith', '11', '2006-08-20', 16),
       (503, 'Alice', 'Johnson', '10', '2007-11-10', 15);
```

![](https://github.com/CLiz17/schoolMockaroo/assets/68838221/2a3294e1-bde2-4e72-a7cb-cdb44022d263)

```bash
INSERT INTO school (name, addr_city, addr_state, addr_pin)
VALUES ('ABC School', 'City', 'State', '12345'),
       ('XYZ School', 'Town', 'State', '67890');
```

![](https://github.com/CLiz17/schoolMockaroo/assets/68838221/a70c694c-5da7-4bf3-a84f-ab4ddf183318)

```bash
INSERT INTO faculty (first_name, last_name, salary, subject, phone_no)
VALUES ('Michael', 'Brown', 50000, 'Mathematics', 1234567890),
       ('Emily', 'Davis', 55000, 'Science', 9876543210);
```

![](https://github.com/CLiz17/schoolMockaroo/assets/68838221/0811e858-fd4e-41ca-b817-aea01e64ab90)
