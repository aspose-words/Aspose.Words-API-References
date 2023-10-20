---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words لـ .NET
description: SaveOptions ExportGeneratorName ملكية. متىحقيقي  يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هيحقيقي  في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

متى`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## أمثلة

يوضح كيفية تعطيل إضافة اسم وإصدار Aspose.Words إلى الملفات المنتجة.

```csharp
Document doc = new Document();

// استخدم https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ لمعرفة كيفية التحقق من النتيجة.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
