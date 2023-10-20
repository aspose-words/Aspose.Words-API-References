---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words لـ .NET
description: HtmlLoadOptions IgnoreNoscriptElements ملكية. الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم تجاهل عناصر HTML noscript أم لا. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم تجاهل عناصر HTML &lt;noscript&gt; أم لا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## ملاحظات

مثل MS Word، لا يدعم Aspose.Words البرامج النصية ويقوم افتراضيًا بتحميل محتوى &lt;noscript&gt; Elements في المستند الناتج. ومع ذلك، في معظم المتصفحات، تكون البرامج النصية مدعومة ولا يكون المحتوى من &lt;noscript&gt; مرئيًا. تعيين هذه الخاصية إلى`حقيقي` يجبر Aspose.Words على تجاهل كافة العناصر &lt;noscript&gt; ويساعد في إنتاج مستندات تبدو أقرب إلى ما يتم رؤيته في المتصفحات.

## أمثلة

يوضح كيفية تجاهل عناصر HTML &lt;noscript&gt;.

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
