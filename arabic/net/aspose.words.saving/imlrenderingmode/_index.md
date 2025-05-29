---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف وضع ImlRenderingMode في Aspose.Words لعرض InkML مثالي. حسّن إخراج مستندك بتصور دقيق لكائنات الحبر!
type: docs
weight: 6000
url: /ar/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

يحدد كيفية عرض كائنات الحبر (InkML) إلى تنسيقات الصفحات الثابتة.

```csharp
public enum ImlRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Fallback | `0` | إذا كان الشكل البديل متاحًا لكائن الحبر (InkML)، يقوم Aspose.Words بعرض الشكل البديل بدلاً من InkML. |
| InkML | `1` | يتجاهل Aspose.Words الشكل الخلفي لكائن الحبر (InkML) ويقوم بعرض InkML نفسه. هذا هو الوضع الافتراضي. |

## أمثلة

يُظهر كيفية عرض كائن الحبر.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// يتجاهل تعيين 'ImlRenderingMode.InkML' الشكل البديل لكائن الحبر (InkML) ويقوم بعرض InkML نفسه.
// إذا كانت نتيجة العرض غير مرضية،
// يرجى استخدام 'ImlRenderingMode.Fallback' للحصول على نتيجة مشابهة للإصدارات السابقة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
