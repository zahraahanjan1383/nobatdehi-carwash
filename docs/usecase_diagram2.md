# Use Case Diagram

```mermaid
  


flowchart TB

    %% تعریف نقش‌ها با شکل و رنگ متفاوت
    A([مشتری]):::actorStyle
    B([اپراتور کارواش]):::actorStyle2
    C([مدیر سیستم]):::actorStyle3

    %% Use Caseها با اشکال مختلف
    UC1((ثبت‌نام/ورود)):::usecaseBlue
    UC2{{انتخاب خدمت}}:::usecaseGreen
    UC3([انتخاب زمان نوبت]):::usecaseYellow
    UC4([پرداخت آنلاین]):::usecaseRed
    UC5((مشاهده نوبت‌ها)):::usecaseBlue
    UC6{{لغو یا ویرایش نوبت}}:::usecaseGreen
    UC7([دریافت رسید]):::usecaseYellow

    UC8((مشاهده لیست نوبت‌ها)):::usecaseBlue
    UC9{{تأیید یا رد نوبت}}:::usecaseGreen
    UC10([ثبت وضعیت انجام خدمت]):::usecaseYellow
    UC11([مدیریت ظرفیت روزانه]):::usecaseRed

    UC12((مدیریت خدمات و قیمت‌گذاری)):::usecaseBlue
    UC13{{مدیریت کاربران}}:::usecaseGreen
    UC14([مشاهده گزارش‌ها]):::usecaseYellow
    UC15([ارسال اعلان‌ها]):::usecaseRed
    UC16((تنظیمات سیستم)):::usecaseBlue

    %% ارتباط‌ها
    A --> UC1
    A --> UC2
    A --> UC3
    A --> UC4
    A --> UC5
    A --> UC6
    A --> UC7

    B --> UC1
    B --> UC8
    B --> UC9
    B --> UC10
    B --> UC11

    C --> UC1
    C --> UC12
    C --> UC13
    C --> UC14
    C --> UC15
    C --> UC16

    UC3 --> UC11
    UC4 --> UC5
    UC9 --> UC5
    UC15 --> UC5

    %% استایل‌ها
    classDef actorStyle fill:#f9f,stroke:#333,stroke-width:2px;
    classDef actorStyle2 fill:#bbf,stroke:#333,stroke-width:2px;
    classDef actorStyle3 fill:#bfb,stroke:#333,stroke-width:2px;

    classDef usecaseBlue fill:#ccf,stroke:#333,stroke-width:1px;
    classDef usecaseGreen fill:#cfc,stroke:#333,stroke-width:1px;
    classDef usecaseYellow fill:#ffc,stroke:#333,stroke-width:1px;
    classDef usecaseRed fill:#fcc,stroke:#333,stroke-width:1px;
