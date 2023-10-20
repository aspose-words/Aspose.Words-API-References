---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions Encoding mülk. HTMLye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değeryeni UTF8Kodlamadoğru BOM ile UTF8 C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

HTML'ye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer:`yeni UTF8Kodlama(doğru)` (BOM ile UTF-8).

```csharp
public Encoding Encoding { get; set; }
```

## Örnekler

Bir belgeyi HTML'ye aktarırken hangi kodlamanın kullanılacağını nasıl ayarlayacağınızı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Varsayılan kodlama UTF-8'dir. Belgemizi farklı bir kodlama kullanarak temsil etmek istiyorsak,
// belirli bir kodlamayı ayarlamak için SaveOptions nesnesini kullanabiliriz.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
