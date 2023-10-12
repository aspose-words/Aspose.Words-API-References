---
title: SaveOptions.ImlRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على قيمة أو تعيينها لتحديد كيفية عرض كائنات الحبر InkML.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

الحصول على قيمة أو تعيينها لتحديد كيفية عرض كائنات الحبر (InkML).

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيInkML .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات صفحات ثابتة.

### أمثلة

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

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


