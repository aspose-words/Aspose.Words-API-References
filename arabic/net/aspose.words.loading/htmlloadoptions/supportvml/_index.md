---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية HtmlLoadOptions SupportVml على تحسين تجربة الويب الخاصة بك من خلال تمكين دعم صورة VML لتحسين جودة الرسومات.
type: docs
weight: 70
url: /ar/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

يحصل على قيمة تشير إلى ما إذا كان سيتم دعم صور VML أم لا أو تعيينها.

```csharp
public bool SupportVml { get; set; }
```

## أمثلة

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// إذا كانت القيمة صحيحة، فإننا نأخذ كود VML في الاعتبار أثناء تحليل المستند المحمّل.
loadOptions.SupportVml = supportVml;

// تحتوي هذه الوثيقة على صورة JPEG ضمن علامات "<!--[if gte vml 1]>"،
// وصورة PNG مختلفة ضمن علامات "<![if !vml]>".
// إذا قمنا بتعيين علامة "SupportVml" إلى "true"، فسوف يقوم Aspose.Words بتحميل ملف JPEG.
// إذا قمنا بتعيين هذا العلم إلى "false"، فسوف يقوم Aspose.Words بتحميل PNG فقط.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
