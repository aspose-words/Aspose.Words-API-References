---
title: Document.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words لـ .NET
description: استرجاع اسم الملف الأصلي لمستندك بسهولة باستخدام خاصية "اسم الملف الأصلي للمستند". حسّن سير عملك وتنظيمك اليوم!
type: docs
weight: 300
url: /ar/net/aspose.words/document/originalfilename/
---
## Document.OriginalFileName property

يحصل على اسم الملف الأصلي للمستند.

```csharp
public string OriginalFileName { get; }
```

## ملاحظات

الإرجاعات`باطل` إذا تم تحميل المستند من مجرى أو تم إنشاؤه فارغًا.

## أمثلة

يوضح كيفية استرداد تفاصيل عملية تحميل المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
