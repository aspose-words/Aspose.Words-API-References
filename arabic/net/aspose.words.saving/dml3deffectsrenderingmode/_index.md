---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين مستنداتك باستخدام Dml3DEffectsRenderingMode في Aspose.Words للحصول على عرض متفوق للأشكال ثلاثية الأبعاد والتأثير البصري.
type: docs
weight: 5650
url: /ar/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

يحدد كيفية عرض تأثيرات الشكل ثلاثي الأبعاد.

```csharp
public enum Dml3DEffectsRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Basic | `0` | عرض خفيف الوزن ومستقر، يعتمد على المحرك الداخلي، ولكن التأثيرات المتقدمة مثل الإضاءة والمواد والتأثيرات الإضافية الأخرى لا يتم عرضها عند استخدام هذا الوضع. يرجى الاطلاع على الوثائق للحصول على التفاصيل. |
| Advanced | `1` | عرض قائمة موسعة من التأثيرات الخاصة بما في ذلك التأثيرات ثلاثية الأبعاد المتقدمة مثل الحواف والإضاءة والمواد. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
