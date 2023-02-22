---
title: Document.DefaultTabStop
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Varsayılan sekme durakları arasındaki aralığı nokta olarak alır veya ayarlar.
type: docs
weight: 90
url: /tr/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Varsayılan sekme durakları arasındaki aralığı (nokta olarak) alır veya ayarlar.

```csharp
public double DefaultTabStop { get; set; }
```

### Örnekler

Sekme durdurma konumları için özel bir aralığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sekme duraklarını her 72 noktada (1 inç) görünecek şekilde ayarlayın.
builder.Document.DefaultTabStop = 72;

// Her sekme karakteri, kendisinden sonraki metni bir sonraki en yakın sekme durağı konumuna yaslar.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Ayrıca bakınız

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


