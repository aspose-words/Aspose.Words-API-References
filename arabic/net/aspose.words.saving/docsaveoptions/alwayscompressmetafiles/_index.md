---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words لـ .NET
description: حسّن إدارة مستنداتك باستخدام خاصية AlwaysCompressMetafiles. حسّن الأداء بالتحكم في ضغط ملفات التعريف لزيادة الكفاءة.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

عندما`خطأ شنيع` ، لا يتم ضغط ملفات التعريف الصغيرة لأسباب تتعلق بالأداء. القيمة الافتراضية هي`حقيقي` ، يتم ضغط جميع الملفات التعريفية بغض النظر عن حجمها.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## أمثلة

يوضح كيفية تغيير ضغط الملفات التعريفية في مستند أثناء الحفظ.

```csharp
// افتح مستندًا يحتوي على صيغة Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// عندما نحفظ مستندًا، لا يتم ضغط الملفات التعريفية الأصغر حجمًا لأسباب تتعلق بالأداء.
// يمكننا تعيين علم في كائن SaveOptions لضغط كل ملف تعريفي عند الحفظ.
//بعض المحررين مثل LibreOffice لا يستطيعون قراءة الملفات التعريفية غير المضغوطة.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### أنظر أيضا

* class [DocSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
