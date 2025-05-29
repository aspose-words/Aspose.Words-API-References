---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ScaleImageToShapeSize في HtmlSaveOptions تحجيم الصور في Aspose.Words لتصدير HTML أو MHTML أو EPUB. حسّن مستنداتك!
type: docs
weight: 470
url: /ar/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

يحدد ما إذا كانت الصور يتم قياسها بواسطة Aspose.Words إلى حجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## ملاحظات

الصورة في مستند مايكروسوفت وورد هي شكل. للشكل حجم، وللصورة image حجمها الخاص. لا ترتبط الأحجام مباشرةً. على سبيل المثال، يمكن أن تكون الصورة 1024×786 بكسل، ولكن الشكل الذي يعرض هذه الصورة يمكن أن يكون 400×300 نقطة.

لعرض صورة في المتصفح، يجب أن يتم قياسها إلى حجم الشكل. `ScaleImageToShapeSize` تتحكم الخاصية في المكان الذي يتم فيه تغيير مقياس image : في Aspose.Words أثناء التصدير إلى HTML أو في المتصفح عند عرض المستند.

متى`ScaleImageToShapeSize` يكون`حقيقي` يتم قياس الصورة باستخدام Aspose.Words باستخدام مقياس عالي الجودة أثناء التصدير إلى HTML. عند`ScaleImageToShapeSize` هو`خطأ شنيع`يتم إخراج الصورة بحجمها الأصلي ويتعين على المتصفح تغيير حجمها.

بشكل عام، تُجري المتصفحات عملية تحجيم سريعة وبطيئة الجودة. ونتيجةً لذلك، ستحصل عادةً على جودة عرض أفضل في المتصفح وحجم ملف أصغر عند`ScaleImageToShapeSize` يكون`حقيقي` ، ولكن جودة الطباعة أفضل والتحويل أسرع عند`ScaleImageToShapeSize` يكون`خطأ شنيع`.

بالإضافة إلى الأشكال التي تحتوي على صور نقطية فردية، يؤثر هذا الخيار أيضًا على أشكال المجموعة المكونة من صور نقطية. إذا`ScaleImageToShapeSize` يكون`خطأ شنيع` ويحتوي شكل المجموعة على صور نقطية ذات دقة جوهرية أعلى من القيمة المحددة في[`ImageResolution`](../imageresolution/)سيؤدي استخدام Aspose.Words إلى زيادة دقة عرض هذه المجموعة. هذا يسمح بالحفاظ على جودة الصور عالية الدقة المجمعة بشكل أفضل عند الحفظ بتنسيق HTML.

## أمثلة

يوضح كيفية تعطيل تغيير مقياس الصور إلى أبعاد شكلها الأصلي عند الحفظ في .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل يحتوي على صورة، ثم اجعل هذا الشكل أصغر بكثير من الصورة.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// سيؤدي حفظ مستند يحتوي على أشكال مع صور إلى HTML إلى إنشاء ملف صورة في نظام الملفات المحلي
// لكل شكل. سيستخدم مستند HTML الناتج وسم <image> للربط بهذه الصور وعرضها.
// عندما نحفظ المستند في HTML، يمكننا تمرير كائن SaveOptions لتحديد
// ما إذا كان سيتم تغيير حجم جميع الصور الموجودة داخل الأشكال إلى أحجام أشكالها.
// تعيين علامة "ScaleImageToShapeSize" إلى "true" سيؤدي إلى تقليص حجم كل صورة
// إلى حجم الشكل الذي يحتويه، بحيث لا تكون الصور المحفوظة أكبر من الحجم المطلوب في المستند.
// سيؤدي تعيين علامة "ScaleImageToShapeSize" إلى "false" إلى الحفاظ على أحجام هذه الصور الأصلية،
// مما سيشغل مساحة أكبر مقابل الحفاظ على جودة الصورة.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### أنظر أيضا

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
