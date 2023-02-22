---
title: Enum ImlRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.ImlRenderingMode تعداد. يحدد كيفية عرض كائنات الحبر InkML لتنسيقات الصفحات الثابتة.
type: docs
weight: 4990
url: /ar/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

يحدد كيفية عرض كائنات الحبر (InkML) لتنسيقات الصفحات الثابتة.

```csharp
public enum ImlRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Fallback | `0` | إذا كان الشكل الخلفي متاحًا لكائن الحبر (InkML) ، فإن Aspose. Words يعرض الشكل الخلفي بدلاً من InkML. |
| InkML | `1` | Aspose.Words يتجاهل الشكل الخلفي لكائن الحبر (InkML) ويعرض InkML نفسه . هذا هو الوضع الافتراضي . |

### أمثلة

يوضح كيفية عرض كائن الحبر.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' يتجاهل الشكل الخلفي لكائن الحبر (InkML) ويعرض InkML نفسه.
// إذا كانت نتيجة العرض غير مرضية ،
// الرجاء استخدام "ImlRenderingMode.Fallback" للحصول على نتيجة مشابهة للإصدارات السابقة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


