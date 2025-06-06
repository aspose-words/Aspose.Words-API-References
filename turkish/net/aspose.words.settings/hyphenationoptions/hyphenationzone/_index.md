---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: .NET için Aspose.Words
description: HyphenationZone özelliğiyle metin düzenini optimize edin. Daha temiz, profesyonel belgeler için sağ kenar boşluğundan tireleme mesafesini kontrol edin.
type: docs
weight: 50
url: /tr/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Kelimeleri tirelemek istemediğiniz sağ kenar boşluğundan 1/20'lik bir noktadan uzaklığı alır veya ayarlar. Bu özellik için varsayılan değer 360'tır (0,25 inç).

```csharp
public int HyphenationZone { get; set; }
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
