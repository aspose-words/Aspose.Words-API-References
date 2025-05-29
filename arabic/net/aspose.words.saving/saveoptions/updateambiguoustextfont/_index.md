---
title: SaveOptions.UpdateAmbiguousTextFont
linktitle: UpdateAmbiguousTextFont
articleTitle: UpdateAmbiguousTextFont
second_title: Aspose.Words لـ .NET
description: حسّن وضوح النص في ملفات PDF باستخدام UpdateAmbiguousTextFont. حسّن دقة عرض الخط بناءً على رموز الأحرف لتحسين قابلية القراءة.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/saveoptions/updateambiguoustextfont/
---
## SaveOptions.UpdateAmbiguousTextFont property

يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم.

```csharp
public bool UpdateAmbiguousTextFont { get; set; }
```

## أمثلة

يوضح كيفية تحديث الخط ليتوافق مع رمز الحرف المستخدم.

```csharp
Document doc = new Document(MyDir + "Special symbol.docx");
Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // أريال

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateAmbiguousTextFont = true;
doc.Save(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // أنجسانا الجديدة
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
