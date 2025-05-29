---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: .NET için Aspose.Words
description: Belgenizin biçimlendirmesini ve düzenini geliştirmek için noktalar halinde hassas sekme aralıkları ayarlamak üzere DefaultTabStop özelliğini nasıl özelleştireceğinizi keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Varsayılan sekme durakları arasındaki aralığı (nokta cinsinden) alır veya ayarlar.

```csharp
public double DefaultTabStop { get; set; }
```

## Örnekler

Sekme durağı konumları için özel bir aralığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sekme duraklarını her 72 noktada (1 inç) görünecek şekilde ayarlayın.
builder.Document.DefaultTabStop = 72;

// Her sekme karakteri kendisinden sonraki metni en yakın sekme durağı konumuna yerleştirir.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Ayrıca bakınız

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
