---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words لـ .NET
description: ChmLoadOptions OriginalFileName ملكية. اسم ملف CHM. القيمة الافتراضية هيباطل  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

اسم ملف CHM. القيمة الافتراضية هي`باطل` .

```csharp
public string OriginalFileName { get; set; }
```

## ملاحظات

قد تحتوي مستندات آلية تبادل المعلومات (CHM) على روابط تشير إلى نفس المستند حسب اسم الملف. يدعم Aspose.Words هذه الروابط ويستخدمها بشكل طبيعي[`OriginalFileName`](../../../aspose.words/document/originalfilename/) للتحقق مما إذا كان الملف المشار إليه بواسطة link هو الملف الذي يتم تحميله. إذا تم تحميل مستند من دفق، فيجب تحديد اسم الملف الأصلي الخاص به بشكل صريح عبر هذه الخاصية، حيث لا يمكن تحديده تلقائيًا.

إذا تم تحميل مستند آلية تبادل المعلومات (CHM) من ملف وتم تحديد قيمة غير فارغة لهذه الخاصية، فستأخذ القيمة أولوية على الاسم الفعلي للملف المخزن في[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## أمثلة

يوضح كيفية حل عناوين URL مثل "ms-its:myfile.chm::/index.htm".

```csharp
// تحتوي وثيقتنا على عناوين URL مثل "ms-its:amhelp.chm::....htm"، ولكن لها اسمًا مختلفًا،
// لذلك لا تعمل روابط الملفات بعد حفظها بتنسيق HTML.
// نحتاج إلى تحديد اسم الملف الأصلي في "ChmLoadOptions" لتجنب هذا السلوك.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### أنظر أيضا

* class [ChmLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
