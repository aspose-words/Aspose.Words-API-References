---
title: HyphenationOptions.HyphenationZone
second_title: Aspose.Words for .NET API Referansı
description: HyphenationOptions mülk. Kelimeleri tirelemek için istemediğiniz sağ kenar boşluğundan bir noktanın 1/20si olarak mesafeyi alır veya ayarlar. Bu özellik için varsayılan değer 360tır 025 inç.
type: docs
weight: 50
url: /tr/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Kelimeleri tirelemek için istemediğiniz sağ kenar boşluğundan bir noktanın 1/20'si olarak mesafeyi alır veya ayarlar. Bu özellik için varsayılan değer 360'tır (0,25 inç).

```csharp
public int HyphenationZone { get; set; }
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


