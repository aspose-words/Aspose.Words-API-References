---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية SaveOptions ImlRenderingMode عرض كائنات InkML. حسّن عرضك بالحبر للحصول على نتائج بصرية أفضل!
type: docs
weight: 90
url: /ar/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

يحصل على قيمة تحدد كيفية عرض كائنات الحبر (InkML) أو يعينها.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيInkML .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات الصفحات الثابتة.

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

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
