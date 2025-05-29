---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words لـ .NET
description: حسّن تصديرات ODT باستخدام خاصية IsStrictSchema11. تأكد من التوافق التام مع إصدار ODT 1.1 أو فعّل التوافق مع الإصدار 1.2 للحصول على أفضل النتائج.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

يحدد ما إذا كان التصدير يجب أن يتوافق مع مواصفات ODT 1.1 بشكل صارم. يعرض OOo 3.0 الملفات بشكل صحيح عندما تحتوي على عناصر وسمات ODT 1.2. استخدم "false" لهذا الغرض، أو "true" للتوافق الصارم مع المواصفات 1.1. القيمة الافتراضية هي`خطأ شنيع` .

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
