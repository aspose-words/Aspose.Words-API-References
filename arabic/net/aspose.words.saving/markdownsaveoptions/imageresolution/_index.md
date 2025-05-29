---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words لـ .NET
description: حسّن تصديرات Markdown باستخدام خاصية ImageResolution، مع ضبط دقة الإخراج المخصصة للحصول على صور أكثر وضوحًا. افتراضيًا، 96 نقطة في البوصة.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

يحدد دقة الإخراج للصور عند التصدير إلى Markdown. الافتراضي هو`96 نقطة في البوصة` .

```csharp
public int ImageResolution { get; set; }
```

## أمثلة

يوضح كيفية ضبط دقة الإخراج للصور.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### أنظر أيضا

* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
