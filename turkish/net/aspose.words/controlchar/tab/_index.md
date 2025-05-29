---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: .NET için Aspose.Words
description: ControlChar Tab alanını keşfedin, verimli metin biçimlendirme ve gelişmiş veri yönetimi için Tab karakteri x0009'u anlayın.
type: docs
weight: 270
url: /tr/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Sekme karakteri: "\x0009" veya "\t".

```csharp
public static readonly string Tab;
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

* class [ControlChar](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
