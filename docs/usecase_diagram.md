#  دیاگرام Use Case پروژه نوبت‌دهی کارواش

این دیاگرام نشون می‌ده که چه نقش‌هایی توی سیستم وجود دارن و هر نقش چه کاری می‌تونه انجام بده. هدفش اینه که تعامل بین کاربرها و سیستم رو تصویری نشون بده تا همه راحت‌تر بفهمن سیستم چطور کار می‌کنه.

##  دیاگرام با استفاده از Mermaid:


# Use Case Diagram

```mermaid
  



flowchart TB

    %% --- Actors ---
    Customer([👤 مشتری]):::actor
    Operator([🧑🔧 اپراتور کارواش]):::actor2
    Admin([🛠 مدیر سیستم]):::actor3

    %% --- Customer Use Cases ---
    UC1((ثبت‌نام / ورود)):::ucBlue
    UC2((انتخاب خدمت)):::ucGreen
    UC3((انتخاب زمان نوبت)):::ucYellow
    UC4((پرداخت آنلاین)):::ucRed
    UC5((مشاهده نوبت‌ها)):::ucBlue
    UC6((لغو / ویرایش نوبت)):::ucGreen
    UC7((دریافت رسید)):::ucYellow

    %% --- Operator Use Cases ---
    UC8((مشاهده لیست نوبت‌ها)):::ucBlue
    UC9((تأیید / رد نوبت)):::ucGreen
    UC10((ثبت وضعیت انجام خدمت)):::ucYellow
    UC11((مدیریت ظرفیت روزانه)):::ucRed

    %% --- Admin Use Cases ---
    UC12((مدیریت خدمات و قیمت‌گذاری)):::ucBlue
    UC13((مدیریت کاربران)):::ucGreen
    UC14((مشاهده گزارش‌ها)):::ucYellow
    UC15((ارسال اعلان‌ها)):::ucRed
    UC16((تنظیمات سیستم)):::ucBlue

    %% --- Relations ---
    Customer --> UC1
    Customer --> UC2
    Customer --> UC3
    Customer --> UC4
    Customer --> UC5
    Customer --> UC6
    Customer --> UC7

    Operator --> UC8
    Operator --> UC9
    Operator --> UC10
    Operator --> UC11

    Admin --> UC12
    Admin --> UC13
    Admin --> UC14
    Admin --> UC15
    Admin --> UC16

    %% --- Internal Relations ---
    UC4 --> UC7
    UC3 --> UC11
    UC9 --> UC8
    UC15 --> UC5

    %% --- Styles ---
    classDef actor fill:#ffe6ff,stroke:#333,stroke-width:2px;
    classDef actor2 fill:#e6e6ff,stroke:#333,stroke-width:2px;
    classDef actor3 fill:#e6ffe6,stroke:#333,stroke-width:2px;

    classDef ucBlue fill:#dce6ff,stroke:#333,stroke-width:1px;
    classDef ucGreen fill:#d9ffe0,stroke:#333,stroke-width:1px;
    classDef ucYellow fill:#fff7cc,stroke:#333,stroke-width:1px;
    classDef ucRed fill:#ffd6d6,stroke:#333,stroke-width:1px;
