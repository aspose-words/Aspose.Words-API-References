---
title: FileFormatUtil.ExtensionToSaveFormat
linktitle: ExtensionToSaveFormat
articleTitle: ExtensionToSaveFormat
second_title: Aspose.Words لـ .NET
description: FileFormatUtil ExtensionToSaveFormat طريقة. تحويل امتداد اسم الملف إلى ملفSaveFormat القيمة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

تحويل امتداد اسم الملف إلى ملف[`SaveFormat`](../../saveformat/) القيمة.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| extension | String | امتداد الملف. يمكن أن يكون مع أو بدون نقطة رائدة. حالة الأحرف. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يلقي إذا كانت المعلمة`باطل`. |

## ملاحظات

إذا تعذر التعرف على الامتداد، فسيتم إرجاعهUnknown.

## أمثلة

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

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
