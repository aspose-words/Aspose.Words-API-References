---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: .NET için Aspose.Words
description: HtmlLoadOptions IgnoreNoscriptElements özelliğinin noscript öğelerini kontrol ederek HTML ayrıştırmanızı nasıl geliştirdiğini keşfedin. Web performansınızı bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

&lt;noscript&gt; HTML öğelerinin yoksayılıp yoksayılmayacağını belirten bir değer alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Notlar

MS Word gibi, Aspose.Words de betikleri desteklemez ve varsayılan olarak &lt;noscript&gt; elements içeriğini sonuç belgesine yükler. Ancak çoğu tarayıcıda betikler desteklenir ve &lt;noscript&gt; içeriği görünmez. Bu özelliği şu şekilde ayarlamak`doğru` Aspose.Words'ün tüm &lt;noscript&gt; öğelerini yok saymasını zorlar ve tarayıcılarda görülenlere daha yakın görünen belgeler üretmeye yardımcı olur.

## Örnekler

&lt;noscript&gt; HTML öğelerinin nasıl göz ardı edileceğini gösterir.

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

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
