---
title: HyphenationOptions.HyphenateCaps
second_title: Aspose.Words for .NET API Referansı
description: HyphenationOptions mülk. Tamamı büyük harflerle yazılan kelimelerin tireli olup olmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeridoğru .
type: docs
weight: 40
url: /tr/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Tamamı büyük harflerle yazılan kelimelerin tireli olup olmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri:`doğru` .

```csharp
public bool HyphenateCaps { get; set; }
```

### Örnekler

Otomatik tirelemenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Ayrıca bakınız

* class [HyphenationOptions](../)
* ad alanı [Aspose.Words.Settings](../../hyphenationoptions/)
* toplantı [Aspose.Words](../../../)


