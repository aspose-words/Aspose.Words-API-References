---
title: Create
second_title: Aspose.Words لمراجع .NET API
description: إنشاء كائن CertificateHolder باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به.
type: docs
weight: 10
url: /ar/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

إنشاء كائن CertificateHolder باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| certBytes | Byte[] | صفيف بايت يحتوي على بيانات من شهادة X.509. |
| password | SecureString | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### قيمة الإرجاع

مثيل CertificateHolder

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | إذا ألقيت **الشهادات** باطل |
| InvalidParameterException | إذا ألقيت **كلمه السر** باطل |
| SecurityException | يتم إلقاؤه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم إلقاؤه في حالة وجود كلمة مرور خاطئة أو ملف تالف. |

### أمثلة

يوضح كيفية إنشاء كائنات CertificateHolder.

```csharp
// فيما يلي أربع طرق لإنشاء كائنات CertificateHolder.
// 1 - قم بتحميل ملف PKCS # 12 في مصفوفة بايت وتطبيق كلمة المرور الخاصة به:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - قم بتحميل ملف PKCS # 12 في مصفوفة بايت ، وقم بتطبيق كلمة مرور آمنة:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// إذا كانت الشهادة تحتوي على مفاتيح خاصة مطابقة للأسماء المستعارة ،
// يمكننا استخدام الأسماء المستعارة لجلب مفاتيح كل منها. أولاً ، سوف نتحقق من وجود أسماء مستعارة صالحة.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 4 - مرر "null" كاسم مستعار من أجل استخدام أول اسم مستعار متاح يقوم بإرجاع مفتاح خاص:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

إنشاء كائن CertificateHolder باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| certBytes | Byte[] | صفيف بايت يحتوي على بيانات من شهادة X.509. |
| password | String | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### قيمة الإرجاع

مثيل CertificateHolder

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | إذا ألقيت **الشهادات** باطل |
| InvalidParameterException | إذا ألقيت **كلمه السر** باطل |
| SecurityException | يتم إلقاؤه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم إلقاؤه في حالة وجود كلمة مرور خاطئة أو ملف تالف. |

### أمثلة

يوضح كيفية إنشاء كائنات CertificateHolder.

```csharp
// فيما يلي أربع طرق لإنشاء كائنات CertificateHolder.
// 1 - قم بتحميل ملف PKCS # 12 في مصفوفة بايت وتطبيق كلمة المرور الخاصة به:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - قم بتحميل ملف PKCS # 12 في مصفوفة بايت ، وقم بتطبيق كلمة مرور آمنة:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// إذا كانت الشهادة تحتوي على مفاتيح خاصة مطابقة للأسماء المستعارة ،
// يمكننا استخدام الأسماء المستعارة لجلب مفاتيح كل منها. أولاً ، سوف نتحقق من وجود أسماء مستعارة صالحة.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 4 - مرر "null" كاسم مستعار من أجل استخدام أول اسم مستعار متاح يقوم بإرجاع مفتاح خاص:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

إنشاء كائن CertificateHolder باستخدام المسار إلى مخزن PKCS12 وكلمة المرور الخاصة به.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الشهادة. |
| password | String | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### قيمة الإرجاع

مثيل CertificateHolder

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | إذا ألقيت **اسم الملف** باطل |
| InvalidParameterException | إذا ألقيت **كلمه السر** باطل |
| SecurityException | يتم إلقاؤه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم إلقاؤه في حالة وجود كلمة مرور خاطئة أو ملف تالف. |

### أمثلة

يوضح كيفية توقيع المستندات رقميًا.

```csharp
// أنشئ شهادة X.509 من متجر PKCS # 12 ، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// أنشئ تعليقًا وتاريخًا سيتم تطبيقه بتوقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// خذ مستندًا غير موقع من نظام الملفات المحلي عبر تدفق ملف ،
// ثم أنشئ نسخة موقعة منه يحددها اسم ملف تدفق ملف الإخراج.
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

إنشاء كائن CertificateHolder باستخدام المسار إلى مخزن PKCS12 وكلمة المرور والاسم المستعار باستخدام المفتاح الخاص والشهادة التي سيتم العثور عليها.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الشهادة. |
| password | String | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |
| alias | String | الاسم المستعار المرتبط بشهادة ومفتاحها الخاص |

### قيمة الإرجاع

مثيل CertificateHolder

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidParameterException | إذا ألقيت **اسم الملف** باطل |
| InvalidParameterException | إذا ألقيت **كلمه السر** باطل |
| SecurityException | يتم إلقاؤه إذا كان متجر PKCS12 لا يحتوي على أسماء مستعارة |
| IOException | يتم إلقاؤه في حالة وجود كلمة مرور خاطئة أو ملف تالف. |
| SecurityException | يتم إلقاؤه إذا لم يكن هناك مفتاح خاص بالاسم المستعار المحدد |

### أمثلة

يوضح كيفية إنشاء كائنات CertificateHolder.

```csharp
// فيما يلي أربع طرق لإنشاء كائنات CertificateHolder.
// 1 - قم بتحميل ملف PKCS # 12 في مصفوفة بايت وتطبيق كلمة المرور الخاصة به:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - قم بتحميل ملف PKCS # 12 في مصفوفة بايت ، وقم بتطبيق كلمة مرور آمنة:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// إذا كانت الشهادة تحتوي على مفاتيح خاصة مطابقة للأسماء المستعارة ،
// يمكننا استخدام الأسماء المستعارة لجلب مفاتيح كل منها. أولاً ، سوف نتحقق من وجود أسماء مستعارة صالحة.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 4 - مرر "null" كاسم مستعار من أجل استخدام أول اسم مستعار متاح يقوم بإرجاع مفتاح خاص:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### أنظر أيضا

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../certificateholder/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
