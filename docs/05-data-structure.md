# Data Structure

## 1. User

This entity is used to store data about users who have access to the system.

**Attributes:**
- user_id
- username
- password
- email

## 2. Well

This entity contains master data for wells used in operations.

**Attributes:**
- sumur_id
- nama_sumur
- kode_sumur

## 3. Well Operational Data

This entity contains the main data that stores well operational results for each period.

**Attributes:**
- id
- user_id (relationship to User)
- sumur_id (relationship to Well)
- tanggal
- debit
- kadar
- jam kerja
- jumlah air

## Relationships Between Entities

- Each well operational data record is linked to one well in the Well master table.
- One user can manage many well operational data records.

## System ERD

<p align="center">
  <img src="./diagrams/ERD.drawio.png" width="600"/>
  <br>
  <em>Well Operational Control System ERD</em>
</p>

This ERD illustrates the database structure of the Well Operational Control System, which consists of three main entities: User, Well, and Well Operational Data.

The relationship used is one-to-many (1:N), where one user can enter many operational data records, and one well can have many operational data records.

The Well Operational Data table serves as a transaction table, while the User and Well tables function as reference tables to maintain data consistency.
