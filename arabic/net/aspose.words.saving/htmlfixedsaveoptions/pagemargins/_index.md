---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words لـ .NET
description: HtmlFixedSaveOptions PageMargins ملكية. يحدد الهوامش حول الصفحات في مستند HTML. يتم قياس قيمة الهوامش بالنقاط ويجب أن تكون مساوية أو أكبر من 0. القيمة الافتراضية هي 10 نقاط في C#.
type: docs
weight: 120
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

يحدد الهوامش حول الصفحات في مستند HTML. يتم قياس قيمة الهوامش بالنقاط ويجب أن تكون مساوية أو أكبر من 0. القيمة الافتراضية هي 10 نقاط.

```csharp
public double PageMargins { get; set; }
```

## ملاحظات

يعتمد على قيمة[`PageHorizontalAlignment`](../pagehorizontalalignment/) ملكية:

* يحدد هوامش الصفحة العلوية والسفلية واليسرى إذا كانت القيمة كذلكLeft .
* يحدد هوامش الصفحة العلوية والسفلية واليمنى إذا كانت القيمة كذلكRight .
* يحدد هوامش الصفحة العلوية والسفلية إذا كانت القيمةCenter .

## أمثلة

يوضح كيفية ضبط هوامش الصفحة عند حفظ مستند بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
