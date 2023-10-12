---
title: HtmlLoadOptions.SupportVml
second_title: Aspose.Words لمراجع .NET API
description: HtmlLoadOptions ملكية. الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم دعم صور VML أم لا.
type: docs
weight: 60
url: /ar/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم دعم صور VML أم لا.

```csharp
public bool SupportVml { get; set; }
```

### أمثلة

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// إذا كانت القيمة صحيحة، فسنأخذ رمز VML في الاعتبار أثناء تحليل المستند الذي تم تحميله.
loadOptions.SupportVml = supportVml;

// يحتوي هذا المستند على صورة JPEG داخل "<!--[if gte vml 1]>" العلامات,
// وصورة PNG مختلفة داخل "<![if !vml]>" العلامات.
// إذا قمنا بتعيين علامة "SupportVml" على "صحيح"، فسيقوم Aspose.Words بتحميل ملف JPEG.
// إذا قمنا بتعيين هذه العلامة على "خطأ"، فسيقوم Aspose.Words بتحميل ملف PNG فقط.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../htmlloadoptions/)
* المجسم [Aspose.Words](../../../)


