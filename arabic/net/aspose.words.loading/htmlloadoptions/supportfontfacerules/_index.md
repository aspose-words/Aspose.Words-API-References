---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words لـ .NET
description: اكتشف دعم خيارات تحميل Html وقواعد واجهة الخط، وتحكّم بتحميل الخطوط بسهولة. عزّز تصميم موقعك الإلكتروني بتمكين خطوط مخصصة لمظهر أنيق.
type: docs
weight: 60
url: /ar/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم دعم قواعد @font-face وما إذا كان سيتم تحميل الخطوط المعلنة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## ملاحظات

إذا تم تمكين هذا الخيار، يتم تحميل الخطوط المعلنة في قواعد @font-face وتضمينها في تعريفات الخطوط للمستند الناتج (انظر[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) هذا يجعل الخطوط المُحمّلة متاحة للعرض، لكن الأمر لا يُمكّن تضمين الخطوط تلقائيًا عند الحفظ. لحفظ المستند بالخطوط المُحمّلة، يجب استخدام الأمر [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) ممتلكات[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) يجب تعيين مجموعة على`حقيقي` .

تنسيقات الخطوط المدعومة هي TTF وEOT وWOFF.

لا يتم دعم قواعد @font-face عند تحميل صور SVG.

## أمثلة

يوضح كيفية تحميل قواعد "@font-face" المعلنة.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
