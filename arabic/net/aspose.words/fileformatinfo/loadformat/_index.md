---
title: FileFormatInfo.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words لـ .NET
description: FileFormatInfo LoadFormat ملكية. الحصول على تنسيق المستند الذي تم اكتشافه في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/fileformatinfo/loadformat/
---
## FileFormatInfo.LoadFormat property

الحصول على تنسيق المستند الذي تم اكتشافه.

```csharp
public LoadFormat LoadFormat { get; }
```

## ملاحظات

عندما يتم تشفير مستند OOXML، لا يمكن التأكد مما إذا كان مستند Excel أو Word أو PowerPoint دون فك تشفيره أولاً، لذا بالنسبة لمستند OOXML المشفر، سترجع هذه الخاصية دائمًاDocx.

## أمثلة

يوضح كيفية استخدام فئة FileFormatUtil للكشف عن تنسيق المستند وتشفيره.

```csharp
Document doc = new Document();

// قم بتكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظها، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف وثيقتنا وحالة التشفير الخاصة به.
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
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// استخدم FileFormatInstance جديد لتأكيد توقيعه.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// يمكننا تحميل التوقيعات الخاصة بالمستند الموقع في مجموعة كهذه والوصول إليها.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

يوضح كيفية استخدام أساليب FileFormatUtil للكشف عن تنسيق المستند.

```csharp
// قم بتحميل مستند من ملف يفتقد امتداد الملف، ثم اكتشف تنسيق الملف الخاص به.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المطابق له.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - تحويل LoadFormat مباشرةً إلى SaveFormat الخاص به:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // قم بتحميل مستند من الدفق، ثم احفظه في ملحق الملف الذي تم اكتشافه تلقائيًا.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### أنظر أيضا

* enum [LoadFormat](../../loadformat/)
* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
