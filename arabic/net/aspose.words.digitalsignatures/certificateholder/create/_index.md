---
title: CertificateHolder.Create
second_title: Aspose.Words لمراجع .NET API
description: CertificateHolder طريقة. ينشئCertificateHolder كائن يستخدم مصفوفة بايت من متجر PKCS12 وكلمة المرور الخاصة به.
type: docs
weight: 10
url: /ar/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

ينشئ[`CertificateHolder`](../) كائن يستخدم مصفوفة بايت من متجر PKCS12 وكلمة المرور الخاصة به.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| certBytes | Byte[] | صفيف بايت يحتوي على بيانات من شهادة X.509. |
| password | SecureString | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### قيمة الإرجاع

مثال على[`CertificateHolder`](../)

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | ألقيت إذا*certBytes* يكون`باطل` |
| InvalidParameterException | ألقيت إذا*password* يكون`باطل` |
| SecurityException | يتم طرحه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم طرحها إذا كانت هناك كلمة مرور خاطئة أو ملف تالف. |

### أمثلة

يوضح كيفية إنشاء كائنات حامل الشهادات.

```csharp
// فيما يلي أربع طرق لإنشاء كائنات حامل الشهادات.
// 1 - تحميل ملف PKCS #12 إلى مصفوفة بايت وتطبيق كلمة المرور الخاصة به:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - قم بتحميل ملف PKCS #12 إلى مصفوفة بايت، ثم قم بتطبيق كلمة مرور آمنة:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// إذا كانت الشهادة تحتوي على مفاتيح خاصة تتوافق مع الأسماء المستعارة،
// يمكننا استخدام الأسماء المستعارة لجلب المفاتيح الخاصة بها. أولاً، سوف نتحقق من وجود أسماء مستعارة صالحة.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - استخدم اسمًا مستعارًا صالحًا:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - قم بتمرير "null" كاسم مستعار لاستخدام أول اسم مستعار متاح يُرجع مفتاحًا خاصًا:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

ينشئ[`CertificateHolder`](../) كائن يستخدم مصفوفة بايت من متجر PKCS12 وكلمة المرور الخاصة به.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| certBytes | Byte[] | صفيف بايت يحتوي على بيانات من شهادة X.509. |
| password | String | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### قيمة الإرجاع

مثال على[`CertificateHolder`](../)

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | ألقيت إذا*certBytes* يكون`باطل` |
| InvalidParameterException | ألقيت إذا*password* يكون`باطل` |
| SecurityException | يتم طرحه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم طرحها إذا كانت هناك كلمة مرور خاطئة أو ملف تالف. |

### أمثلة

يوضح كيفية إنشاء كائنات حامل الشهادات.

```csharp
// فيما يلي أربع طرق لإنشاء كائنات حامل الشهادات.
// 1 - تحميل ملف PKCS #12 إلى مصفوفة بايت وتطبيق كلمة المرور الخاصة به:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - قم بتحميل ملف PKCS #12 إلى مصفوفة بايت، ثم قم بتطبيق كلمة مرور آمنة:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// إذا كانت الشهادة تحتوي على مفاتيح خاصة تتوافق مع الأسماء المستعارة،
// يمكننا استخدام الأسماء المستعارة لجلب المفاتيح الخاصة بها. أولاً، سوف نتحقق من وجود أسماء مستعارة صالحة.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - استخدم اسمًا مستعارًا صالحًا:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - قم بتمرير "null" كاسم مستعار لاستخدام أول اسم مستعار متاح يُرجع مفتاحًا خاصًا:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

ينشئ[`CertificateHolder`](../) كائن يستخدم المسار إلى متجر PKCS12 وكلمة المرور الخاصة به.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الشهادة. |
| password | String | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### قيمة الإرجاع

مثال على[`CertificateHolder`](../)

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | ألقيت إذا*fileName* يكون`باطل` |
| InvalidParameterException | ألقيت إذا*password* يكون`باطل` |
| SecurityException | يتم طرحه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم طرحها إذا كانت هناك كلمة مرور خاطئة أو ملف تالف. |

### أمثلة

يوضح كيفية توقيع المستندات رقميًا.

```csharp
// أنشئ شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء تعليق وتاريخ سيتم تطبيقه مع توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// خذ مستندًا غير موقع من نظام الملفات المحلي عبر دفق الملفات،
// ثم قم بإنشاء نسخة موقعة منه يحددها اسم ملف دفق ملف الإخراج.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

ينشئ[`CertificateHolder`](../) كائن يستخدم المسار إلى متجر PKCS12 وكلمة المرور الخاصة به والاسم المستعار باستخدام المفتاح الخاص والشهادة التي سيتم العثور عليها.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الشهادة. |
| password | String | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |
| alias | String | الاسم المستعار المرتبط بالشهادة ومفتاحها الخاص |

### قيمة الإرجاع

مثال على[`CertificateHolder`](../)

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | ألقيت إذا*fileName* يكون`باطل` |
| InvalidParameterException | ألقيت إذا*password* يكون`باطل` |
| SecurityException | يتم طرحه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم طرحها إذا كانت هناك كلمة مرور خاطئة أو ملف تالف. |
| SecurityException | يتم طرحه إذا لم يكن هناك مفتاح خاص بالاسم المستعار المحدد |

### أمثلة

يوضح كيفية إنشاء كائنات حامل الشهادات.

```csharp
// فيما يلي أربع طرق لإنشاء كائنات حامل الشهادات.
// 1 - تحميل ملف PKCS #12 إلى مصفوفة بايت وتطبيق كلمة المرور الخاصة به:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - قم بتحميل ملف PKCS #12 إلى مصفوفة بايت، ثم قم بتطبيق كلمة مرور آمنة:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// إذا كانت الشهادة تحتوي على مفاتيح خاصة تتوافق مع الأسماء المستعارة،
// يمكننا استخدام الأسماء المستعارة لجلب المفاتيح الخاصة بها. أولاً، سوف نتحقق من وجود أسماء مستعارة صالحة.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - استخدم اسمًا مستعارًا صالحًا:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - قم بتمرير "null" كاسم مستعار لاستخدام أول اسم مستعار متاح يُرجع مفتاحًا خاصًا:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)


