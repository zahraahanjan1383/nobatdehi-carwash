```mermaid
classDiagram
    class Customer {
        customerId
        name
        phone
    }

    class Appointment {
        appointmentId
        date
        time
        status
    }

    class Payment {
        paymentId
        amount
        status
    }

    class Admin {
        adminId
        name
    }

    Customer "1" --> "many" Appointment
    Appointment --> Payment
    Admin --> Appointment
