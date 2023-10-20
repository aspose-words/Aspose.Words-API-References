---
title: FileFormatUtil.SaveFormatToExtension
linktitle: SaveFormatToExtension
articleTitle: SaveFormatToExtension
second_title: Aspose.Words لـ .NET
description: FileFormatUtil SaveFormatToExtension طريقة. تحويل قيمة تعداد تنسيق الحفظ إلى امتداد الملف. الامتداد الذي تم إرجاعه عبارة عن سلسلة صغيرة ذات نقطة بادئة في C#.
type: docs
weight: 80
url: /ar/net/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil.SaveFormatToExtension method

تحويل قيمة تعداد تنسيق الحفظ إلى امتداد الملف. الامتداد الذي تم إرجاعه عبارة عن سلسلة صغيرة ذات نقطة بادئة.

```csharp
public static string SaveFormatToExtension(SaveFormat saveFormat)
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | يرمي عندما لا يمكن تحويل. |

## ملاحظات

الWordML يتم تحويل القيمة إلى ".wml".

الFlatOpc يتم تحويل القيمة إلى ".fopc".

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
