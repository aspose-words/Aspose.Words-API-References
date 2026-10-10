---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize"
linktitle: "get_ScaleImageToShapeSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize. يحدد ما إذا كانت الصور تُقاس بواسطة Aspose.Words إلى حجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **true** في C++."
type: docs
weight: 46000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


يحدد ما إذا كانت الصور تُقاس بواسطة Aspose.Words إلى حجم الشكل المحدد عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## ملاحظات


صورة في مستند Microsoft Word هي شكل. الشكل له حجم والصورة لها حجمها الخاص. الأحجام ليست مرتبطة مباشرة. على سبيل المثال، يمكن أن تكون الصورة 1024x786 بكسل، لكن الشكل الذي يعرض هذه الصورة قد يكون 400x300 نقطة.

لعرض صورة في المتصفح، يجب تحجيمها إلى حجم الشكل. الخاصية [ScaleImageToShapeSize](./) تتحكم في مكان حدوث تحجيم الصورة: في Aspose.Words أثناء التصدير إلى HTML أو في المتصفح عند عرض المستند.

عندما يكون [ScaleImageToShapeSize](./) **true**، يتم تحجيم الصورة بواسطة [Aspose.Words](../../../aspose.words/) باستخدام تحجيم عالي الجودة أثناء التصدير إلى HTML. عندما يكون [ScaleImageToShapeSize](./) **false**، تُخرج الصورة بحجمها الأصلي ويجب على المتصفح تحجيمها.

بشكل عام، تقوم المتصفحات بعملية تحجيم سريعة وبجودة منخفضة. نتيجة لذلك، ستحصل عادةً على جودة عرض أفضل في المتصفح وحجم ملف أصغر عندما يكون [ScaleImageToShapeSize](./) **true**، ولكن جودة طباعة أفضل وتحويل أسرع عندما يكون [ScaleImageToShapeSize](./) **false**.

بالإضافة إلى الأشكال التي تحتوي على صور نقطية فردية، يؤثر هذا الخيار أيضًا على الأشكال الجماعية التي تتكون من صور نقطية. إذا كان [ScaleImageToShapeSize](./) **false** وكانت الشكل الجماعي يحتوي على صور نقطية ذات دقة داخلية أعلى من القيمة المحددة في [ImageResolution](../get_imageresolution/)، سيزيد Aspose.Words من دقة العرض لهذا المجموعة. هذا يسمح بالحفاظ بشكل أفضل على جودة الصور عالية الدقة المجمعة عند الحفظ بصيغة HTML.

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
