---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: .NET için Aspose.Words
description: Sorunsuz HTML dışa aktarımları için HtmlFixedSaveOptions Kodlama özelliğini keşfedin. En iyi veri bütünlüğü için BOM ile UTF-8 kodlamasını kolayca ayarlayın.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

HTML'ye aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer`yeni UTF8Kodlama(true)` (BOM ile UTF-8).

```csharp
public Encoding Encoding { get; set; }
```

## Örnekler

Bir belgeyi HTML'e aktarırken hangi kodlamanın kullanılacağını nasıl ayarlayacağınızı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Varsayılan kodlama UTF-8'dir. Belgemizi farklı bir kodlama kullanarak temsil etmek istiyorsak,
// Belirli bir kodlamayı ayarlamak için SaveOptions nesnesini kullanabiliriz.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
