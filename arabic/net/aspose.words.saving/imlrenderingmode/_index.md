---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.ImlRenderingMode تعداد. يحدد كيفية عرض كائنات الحبر InkML إلى تنسيقات الصفحات الثابتة في C#.
type: docs
weight: 5250
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
| Fallback | `0` | إذا كان الشكل الاحتياطي متاحًا لكائن الحبر (InkML)، فإن Aspose.Words يعرض الشكل الاحتياطي بدلاً من InkML. |
| InkML | `1` | يتجاهل Aspose.Words الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه. هذا هو الوضع الافتراضي. |

## أمثلة

يوضح كيفية تقديم كائن الحبر.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' يتجاهل الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه.
// إذا كانت نتيجة العرض غير مرضية،
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
