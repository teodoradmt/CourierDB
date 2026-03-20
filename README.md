#  CourierDB

## Overview

CourierDB is a MongoDB-based database project designed to manage courier service operations.
It includes functionality for handling customers, packages, couriers and payment.

---

##  Features

* Manage customers and their details
* Track packages and delivery statuses
* Store courier information (region, vehicle type, etc.)
* Use aggregation pipelines for data analysis
* Perform joins between collections using `$lookup`

---

##  Collections

###  Customers

* customerId
* firstName
* lastName
* phone
* email
* city
* address
* isBusinessClient
* createdAt

###  Packages

* packageId
* trackingNumber
* status
* price
* courierId
* customerId
* statusHistory

###  Couriers

* courierId
* firstName
* lastName
* region
* vehicleType

###  Offices 

* officeId
* city
* workingHours

---

##  Relationships

* A **customer** can have multiple packages
* A **courier** delivers multiple packages
* Relationships are implemented using `$lookup`

---

##  Technologies Used

* MongoDB
* MongoDB Compass
* Aggregation Framework

---

##  Notes

* The project demonstrates NoSQL data modeling techniques
* Focuses on aggregation pipelines and relationships
* Includes both built-in MongoDB roles (for example read, readWrite, dbOwner, adminUser etc.) and custom roles such as employeeReader and employeeWriter
* Authentication is configured via the MongoDB configuration file (mongod.cfg) and changes <u>require</u> restarting MongoDB from Services
* Аggregation pipelines are easily created and tested using MongoDB Compass, with the option to export the generated code and use it in MongoDB shell
* Designed for educational purposes


---

##  Author

Teodora Dimitrova
