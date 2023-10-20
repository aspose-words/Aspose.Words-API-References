---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words لـ .NET
description: OdtSaveOptions IsStrictSchema11 ملكية. يحدد ما إذا كان يجب أن يتوافق التصدير مع مواصفات ODT 1.1 بدقة. OOo 3.0 يعرض الملفات بشكل صحيح عندما تحتوي على عناصر وسمات ODT 1.2. استخدم خطأ لهذا الغرض أو صحيح للمطابقة الصارمة للمواصفات 1.1. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

يحدد ما إذا كان يجب أن يتوافق التصدير مع مواصفات ODT 1.1 بدقة. OOo 3.0 يعرض الملفات بشكل صحيح عندما تحتوي على عناصر وسمات ODT 1.2. استخدم "خطأ" لهذا الغرض، أو "صحيح" للمطابقة الصارمة للمواصفات 1.1. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IsStrictSchema11 { get; set; }
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

* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
