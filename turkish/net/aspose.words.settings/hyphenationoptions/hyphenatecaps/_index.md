---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: .NET için Aspose.Words
description: HyphenationOptions'daki HyphenateCaps özelliğini keşfedin. Tümü büyük harflerle yazılmış kelimeler için tirelemeyi kolayca kontrol edin; varsayılan ayar true'dur. Metninizi bugün optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Tümü büyük harflerle yazılmış kelimelerin tireli olup olmadığını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer`doğru` .

```csharp
public bool HyphenateCaps { get; set; }
```

## Örnekler

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
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
