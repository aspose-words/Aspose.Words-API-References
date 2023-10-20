---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words لـ .NET
description: DocSaveOptions AlwaysCompressMetafiles ملكية. متىخطأ شنيع  لا يتم ضغط ملفات التعريف الصغيرة لأسباب تتعلق بالأداء. القيمة الافتراضية هيحقيقي يتم ضغط كافة ملفات التعريف بغض النظر عن حجمها في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

متى`خطأ شنيع` ، لا يتم ضغط ملفات التعريف الصغيرة لأسباب تتعلق بالأداء. القيمة الافتراضية هي`حقيقي` يتم ضغط كافة ملفات التعريف بغض النظر عن حجمها.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## أمثلة

يوضح كيفية تغيير ضغط ملفات التعريف في مستند أثناء الحفظ.

```csharp
// افتح مستندًا يحتوي على صيغة Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// عندما نحفظ مستندًا، لا يتم ضغط ملفات التعريف الأصغر لأسباب تتعلق بالأداء.
// يمكننا تعيين علامة في كائن SaveOptions لضغط كل ملف تعريف عند الحفظ.
// لا يستطيع بعض المحررين مثل LibreOffice قراءة ملفات التعريف غير المضغوطة.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
    Assert.That(10000, Is.LessThan(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
else
    Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
```

### أنظر أيضا

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
