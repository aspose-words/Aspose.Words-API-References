---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.MeasurementUnits enum لاختيار وحدات القياس بدقة في معالجة المستندات. حسّن سير عملك بخيارات قياس دقيقة!
type: docs
weight: 4840
url: /ar/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

يحدد وحدة القياس.

```csharp
public enum MeasurementUnits
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Inches | `0` | بوصة. |
| Centimeters | `1` | سنتيمتر. |
| Millimeters | `2` | ملليمتر. |
| Points | `3` | نقاط. |
| Picas | `4` | Picas (تستخدم عادةً في المسافات بين الخطوط في الآلة الكاتبة التقليدية). |

## أمثلة

يوضح كيفية جعل المستند المحفوظ يتوافق مع مخطط ODT الأقدم.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
