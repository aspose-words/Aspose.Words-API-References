---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية HtmlLoadOptions IgnoreNoscriptElements تحليل HTML لديك من خلال التحكم في عناصر noscript. حسّن أداء موقعك الإلكتروني اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم تجاهل عناصر HTML &lt;noscript&gt;. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## ملاحظات

مثل مايكروسوفت وورد، لا يدعم Aspose.Words البرامج النصية، ويُحمّل افتراضيًا محتوى عناصر &lt;noscript&gt; في المستند الناتج. مع ذلك، تدعم معظم المتصفحات البرامج النصية، ولا يظهر محتوى &lt;noscript&gt; . يؤدي ضبط هذه الخاصية إلى`حقيقي` يجبر Aspose.Words على تجاهل جميع عناصر &lt;noscript&gt; ويساعد في إنتاج مستندات تبدو أقرب إلى ما يتم رؤيته في المتصفحات.

## أمثلة

يوضح كيفية تجاهل عناصر &lt;noscript&gt; HTML.

```csharp
const string html = @"
    <html>
      <head>
        <title>NOSCRIPT</title>
          <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">
          <script type=""text/javascript"">
            alert(""Hello, world!"");
          </script>
      </head>
    <body>
      <noscript><p>Your browser does not support JavaScript!</p></noscript>
    </body>
    </html>";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.IgnoreNoscriptElements = ignoreNoscriptElements;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
