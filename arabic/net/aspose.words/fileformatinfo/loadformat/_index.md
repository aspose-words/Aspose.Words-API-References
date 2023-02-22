---
title: FileFormatInfo.LoadFormat
second_title: Aspose.Words لمراجع .NET API
description: FileFormatInfo ملكية. يحصل على تنسيق المستند المكتشف.
type: docs
weight: 40
url: /ar/net/aspose.words/fileformatinfo/loadformat/
---
## FileFormatInfo.LoadFormat property

يحصل على تنسيق المستند المكتشف.

```csharp
public LoadFormat LoadFormat { get; }
```

### ملاحظات

عندما يتم تشفير مستند OOXML ، لا يمكن التأكد مما إذا كان مستند Excel أو Word أو PowerPoint دون فك تشفيره أولاً ، لذا بالنسبة لمستند OOXML المشفر ، ستعود هذه الخاصية دائمًاDocx.

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../fileformatinfo/)
* المجسم [Aspose.Words](../../../)


