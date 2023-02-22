---
title: HtmlFixedSaveOptions.Encoding
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. HTMLye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değeryeni UTF8Encodingdoğru BOM ile UTF8.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

HTML'ye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer`yeni UTF8Encoding(doğru)` (BOM ile UTF-8).

```csharp
public Encoding Encoding { get; set; }
```

### Örnekler

Bir belgeyi HTML'ye dışa aktarırken hangi kodlamanın kullanılacağını nasıl ayarlayacağınızı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Varsayılan kodlama UTF-8'dir. Belgemizi farklı bir kodlama ile temsil etmek istiyorsak,
// belirli bir kodlama ayarlamak için SaveOptions nesnesini kullanabiliriz.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


