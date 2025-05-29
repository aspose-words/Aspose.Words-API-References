---
title: SaveOptions.Dml3DEffectsRenderingMode
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveOptions Dml3DEffectsRenderingMode للتحكم بسهولة في عرض التأثير ثلاثي الأبعاد لتحسين جودة الصورة في تطبيقاتك.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/saveoptions/dml3deffectsrenderingmode/
---
## SaveOptions.Dml3DEffectsRenderingMode property

يحصل على قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد أو يعينها.

```csharp
public Dml3DEffectsRenderingMode Dml3DEffectsRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيBasic .

## أمثلة

يُظهر كيفية تقديم التأثيرات ثلاثية الأبعاد.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### أنظر أيضا

* enum [Dml3DEffectsRenderingMode](../../dml3deffectsrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
