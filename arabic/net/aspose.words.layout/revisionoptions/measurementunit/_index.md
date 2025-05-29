---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words لـ .NET
description: خصّص تعليقاتك على المراجعات باستخدام خاصية وحدة القياس في خيارات المراجعة. حدّد وحدات القياس بسهولة، مع اختيار السنتيمترات كوحدة افتراضية.
type: docs
weight: 80
url: /ar/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

يسمح بتحديد وحدات القياس لتعليقات المراجعة. القيمة الافتراضية هيCentimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

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

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
