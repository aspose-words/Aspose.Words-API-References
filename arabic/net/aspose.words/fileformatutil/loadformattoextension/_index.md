---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: Aspose.Words لـ .NET
description: حوّل قيم تنسيق التحميل إلى امتدادات ملفات بسهولة باستخدام طريقة LoadFormatToExtension من FileFormatUtil. احصل على امتدادات دقيقة بأحرف صغيرة بسهولة!
type: docs
weight: 60
url: /ar/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

يُحوِّل قيمة مُعَدَّة بتنسيق تحميل إلى امتداد ملف. الامتداد المُعاد هو سلسلة نصية صغيرة تُستهل بنقطة.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | يرمي عندما لا يمكن التحويل. |

## ملاحظات

الWordML يتم تحويل القيمة إلى ".wml".

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
