```mermaid
stateDiagram
    [*] --> Requested
    Requested --> Paid : پرداخت موفق
    Requested --> Canceled : لغو توسط مشتری
    Paid --> Completed : انجام سرویس
    Paid --> Refunded : بازگشت وجه
    Canceled --> [*]
    Completed --> [*]
    Refunded --> [*]
