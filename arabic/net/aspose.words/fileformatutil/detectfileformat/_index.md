---
title: FileFormatUtil.DetectFileFormat
second_title: Aspose.Words لمراجع .NET API
description: FileFormatUtil طريقة. يكتشف ويعيد المعلومات المتعلقة بتنسيق مستند مخزن في ملف قرص.
type: docs
weight: 30
url: /ar/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(string) {#detectfileformat_1}

يكتشف ويعيد المعلومات المتعلقة بتنسيق مستند مخزن في ملف قرص.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف. |

### قيمة الإرجاع

أ[`FileFormatInfo`](../../fileformatinfo/) الكائن الذي يحتوي على المعلومات المكتشفة.

### ملاحظات

حتى إذا اكتشفت هذه الطريقة تنسيق المستند ، فإنها لا تضمن أن المستند المحدد صالح. تكتشف هذه الطريقة تنسيق المستند فقط عن طريق قراءة البيانات الكافية للكشف عن . للتحقق الكامل من صلاحية المستند ، يلزمك تحميل المستند في ملف[`Document`](../../document/) هدف.

هذه الطريقة ترمي[`FileCorruptedException`](../../filecorruptedexception/) عندما يتم التعرف على التنسيق ، ولكن لا يمكن إكمال الاكتشاف بسبب التلف.

### أمثلة

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند وتشفيره.

```csharp
Document doc = new Document();

// تكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظها ، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف وثيقتنا ، وحالة تشفيرها.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.

```csharp
// استخدم مثيل FileFormatInfo للتحقق من عدم توقيع المستند رقميًا.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// استخدم FileFormatInstance جديدًا لتأكيد توقيعه.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// يمكننا تحميل والوصول إلى توقيعات وثيقة موقعة في مجموعة مثل هذه.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### أنظر أيضا

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../fileformatutil/)
* المجسم [Aspose.Words](../../../)

---

## DetectFileFormat(Stream) {#detectfileformat}

يكتشف ويعيد المعلومات المتعلقة بتنسيق مستند مخزّن في تدفق.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق. |

### قيمة الإرجاع

أ[`FileFormatInfo`](../../fileformatinfo/) الكائن الذي يحتوي على المعلومات المكتشفة.

### ملاحظات

يجب وضع الدفق في بداية المستند.

عندما تعود هذه الطريقة ، تتم استعادة الموضع في الدفق إلى الموضع الأصلي.

حتى إذا اكتشفت هذه الطريقة تنسيق المستند ، فإنها لا تضمن أن المستند المحدد صالح. تكتشف هذه الطريقة تنسيق المستند فقط عن طريق قراءة البيانات الكافية للكشف عن . للتحقق الكامل من صلاحية المستند ، يلزمك تحميل المستند في ملف[`Document`](../../document/) هدف.

هذه الطريقة ترمي[`FileCorruptedException`](../../filecorruptedexception/) عندما يتم التعرف على التنسيق ، ولكن لا يمكن إكمال الاكتشاف بسبب التلف.

### أمثلة

يوضح كيفية استخدام أساليب FileFormatUtil لاكتشاف تنسيق المستند.

```csharp
// قم بتحميل مستند من ملف يفتقد إلى امتداد الملف ، ثم اكتشف تنسيق الملف الخاص به.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المقابل له.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat ، ثم احصل على تنسيق SaveFormat المقابل من تلك السلسلة:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - تحويل LoadFormat مباشرة إلى SaveFormat الخاص به:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // قم بتحميل مستند من الدفق ، ثم احفظه في امتداد الملف المكتشف تلقائيًا.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### أنظر أيضا

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../fileformatutil/)
* المجسم [Aspose.Words](../../../)


