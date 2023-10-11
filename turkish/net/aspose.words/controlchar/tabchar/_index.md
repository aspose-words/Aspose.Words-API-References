---
title: ControlChar.TabChar
second_title: Aspose.Words for .NET API Referansı
description: ControlChar alan. Sekme karakteri char9 veya t.
type: docs
weight: 280
url: /tr/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Sekme karakteri: (char)9 veya "\t".

```csharp
public const char TabChar;
```

### Örnekler

Sekme durağı konumları için özel aralığın nasıl ayarlanacağını gösterir.

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

* class [ControlChar](../)
* ad alanı [Aspose.Words](../../controlchar/)
* toplantı [Aspose.Words](../../../)


