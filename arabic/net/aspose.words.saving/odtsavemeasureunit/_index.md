---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.OdtSaveMeasureUnit تعداد. وحدات قياس محددة لتطبيقها على محتوى المستند القابل للقياس مثل الشكل والعروض وغيرها أثناء الحفظ في C#.
type: docs
weight: 5320
url: /ar/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

وحدات قياس محددة لتطبيقها على محتوى المستند القابل للقياس مثل الشكل والعروض وغيرها أثناء الحفظ.

```csharp
public enum OdtSaveMeasureUnit
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Centimeters | `0` | يحدد حفظ محتوى المستند باستخدام السنتيمترات. |
| Inches | `1` | يحدد حفظ محتوى المستند بالبوصة. |

## أمثلة

يوضح كيفية استخدام وحدات قياس مختلفة لتحديد معلمات النمط لمستند ODT المحفوظ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نقوم بتصدير المستند إلى .odt، يمكننا استخدام كائن OdtSaveOptions لتعديل كيفية حفظ المستند.
// يمكننا ضبط خاصية "MeasureUnit" على "OdtSaveMeasureUnit.Centimeters"
 // لتحديد المحتوى مثل معلمات النمط باستخدام النظام المتري الذي يستخدمه Open Office.
// يمكننا ضبط خاصية "MeasureUnit" على "OdtSaveMeasureUnit.Inches"
// لتحديد المحتوى مثل معلمات النمط باستخدام النظام الإمبراطوري الذي يستخدمه Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
