---
title: HyphenationOptions.AutoHyphenation
linktitle: AutoHyphenation
articleTitle: AutoHyphenation
second_title: .NET için Aspose.Words
description: HyphenationOptions özelliğiyle otomatik tirelemeyi kontrol edin. Bu özelliği açıp kapatarak belgenizin okunabilirliğini kolayca artırın.
type: docs
weight: 20
url: /tr/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` .

```csharp
public bool AutoHyphenation { get; set; }
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
