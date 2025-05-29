---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım ve kullanıcı deneyimi için tablonuzun düzenini kolayca ayarlamak ve optimize etmek amacıyla Table PreferredWidth özelliğini nasıl kullanacağınızı keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Tablonun tercih edilen genişliğini alır veya ayarlar.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Notlar

Varsayılan değer:[`Auto`](../../preferredwidth/auto/).

## Örnekler

Bir tablonun sayfa genişliğinin %50'sine otomatik olarak sığacak şekilde nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### Ayrıca bakınız

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
