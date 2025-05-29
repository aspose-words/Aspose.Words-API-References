---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.OdtSaveMeasureUnit للتحكم الدقيق في قياسات المستندات. حسّن تنسيق مستنداتك بسهولة!
type: docs
weight: 6100
url: /ar/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

وحدات قياس محددة لتطبيقها على محتوى المستند القابل للقياس مثل الشكل والعرض وغير ذلك أثناء الحفظ.

```csharp
public enum OdtSaveMeasureUnit
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Centimeters | `0` | يحدد أن محتوى المستند يتم حفظه باستخدام السنتيمترات. |
| Inches | `1` | يحدد أن محتوى المستند يتم حفظه باستخدام البوصات. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
