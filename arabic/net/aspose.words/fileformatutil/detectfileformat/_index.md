---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words لـ .NET
description: حدّد تنسيقات المستندات بسرعة باستخدام أداة DetectFileFormat من FileFormatUtil. احصل على تحليلات دقيقة للتنسيقات لإدارة ملفات فعّالة.
type: docs
weight: 30
url: /ar/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

يكتشف ويعيد المعلومات حول تنسيق المستند المخزن في ملف القرص.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف. |

### قيمة الإرجاع

أ[`FileFormatInfo`](../../fileformatinfo/) الكائن الذي يحتوي على المعلومات المكتشفة.

## ملاحظات

حتى لو اكتشفت هذه الطريقة تنسيق المستند، فإنها لا تضمن صحة المستند المحدد. تكتشف هذه الطريقة تنسيق المستند فقط من خلال قراءة البيانات الكافية للكشف. للتحقق تمامًا من صحة المستند، يجب تحميله إلى[`Document`](../../document/) هدف.

هذه الطريقة ترمي[`FileCorruptedException`](../../filecorruptedexception/) عندما يتم التعرف على التنسيق is ، ولكن لا يمكن إكمال عملية الاكتشاف بسبب الفساد.

## أمثلة

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند والتشفير.

```csharp
Document doc = new Document();

// تكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظه، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// التحقق من نوع الملف الخاص بمستندنا وحالة تشفيره.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

يوضح كيفية استخدام فئة FileFormatUtil للكشف عن تنسيق المستند ووجود التوقيعات الرقمية.

```csharp
// استخدم مثيل FileFormatInfo للتحقق من عدم توقيع المستند رقميًا.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// استخدم FileFormatInstance جديدًا للتأكد من توقيعه.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// يمكننا تحميل التوقيعات الخاصة بمستند موقّع والوصول إليها في مجموعة مثل هذه.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### أنظر أيضا

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

يكتشف ويعيد المعلومات حول تنسيق المستند المخزن في مجرى.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | النهر. |

### قيمة الإرجاع

أ[`FileFormatInfo`](../../fileformatinfo/) الكائن الذي يحتوي على المعلومات المكتشفة.

## ملاحظات

يجب وضع الدفق في بداية المستند.

عندما تعود هذه الطريقة، يتم استعادة الموضع في الدفق إلى الموضع الأصلي.

حتى لو اكتشفت هذه الطريقة تنسيق المستند، فإنها لا تضمن صحة المستند المحدد. تكتشف هذه الطريقة تنسيق المستند فقط من خلال قراءة البيانات الكافية للكشف. للتحقق تمامًا من صحة المستند، يجب تحميله إلى[`Document`](../../document/) هدف.

هذه الطريقة ترمي[`FileCorruptedException`](../../filecorruptedexception/) عندما يتم التعرف على التنسيق is ، ولكن لا يمكن إكمال عملية الاكتشاف بسبب الفساد.

## أمثلة

يوضح كيفية استخدام طرق FileFormatUtil للكشف عن تنسيق المستند.

```csharp
// قم بتحميل مستند من ملف يفتقد ملحق الملف، ثم اكتشف تنسيق الملف الخاص به.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المقابل له.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - تحويل LoadFormat مباشرة إلى SaveFormat الخاص به:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // قم بتحميل مستند من الدفق، ثم احفظه في امتداد الملف الذي تم اكتشافه تلقائيًا.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### أنظر أيضا

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
