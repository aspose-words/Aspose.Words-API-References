---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words لـ .NET
description: خصّص وحدة القياس في مستندك باستخدام خيارات OdtSaveOptions. اختر وحدات القياس المُفضّلة لديك للدقة - الافتراضي هو السنتيمترات.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

يسمح بتحديد وحدات القياس التي سيتم تطبيقها على محتوى المستند. القيمة الافتراضية هيCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## ملاحظات

يستخدم Open Office السنتيمترات عند تحديد الأطوال والعروض وتنسيقات أخرى قابلة للقياس وخصائص المحتوى في المستندات بينما يستخدم MS Office البوصات.

## أمثلة

يوضح كيفية استخدام وحدات القياس المختلفة لتحديد معلمات النمط لمستند ODT المحفوظ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نقوم بتصدير المستند إلى .odt، يمكننا استخدام كائن OdtSaveOptions لتعديل كيفية حفظ المستند.
// يمكننا تعيين خاصية "MeasureUnit" إلى "OdtSaveMeasureUnit.Centimeters"
 // لتحديد المحتوى مثل معلمات النمط باستخدام النظام المتري الذي يستخدمه Open Office.
// يمكننا تعيين خاصية "MeasureUnit" إلى "OdtSaveMeasureUnit.Inches"
// لتحديد المحتوى مثل معلمات النمط باستخدام النظام الإمبراطوري الذي يستخدمه Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### أنظر أيضا

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
