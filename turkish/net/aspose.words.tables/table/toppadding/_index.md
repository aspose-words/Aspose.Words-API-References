---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words for .NET
description: Table TopPadding mülk. Hücre içeriğinin üzerine eklenecek alan miktarını puan cinsinden alır veya ayarlar C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

Hücre içeriğinin üzerine eklenecek alan miktarını (puan cinsinden) alır veya ayarlar.

```csharp
public double TopPadding { get; set; }
```

## Örnekler

Bir tabloda içerik dolgusunun nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Tablodaki her hücre için, içeriği ile kenarlıkları arasındaki mesafeyi ayarlayın.
// Bu tablo, metni kaydırarak minimum dolgu mesafesini koruyacaktır.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
