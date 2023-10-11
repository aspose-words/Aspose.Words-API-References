---
title: Table.RightPadding
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. Hücre içeriğinin sağına eklenecek alan miktarını puan cinsinden alır veya ayarlar.
type: docs
weight: 250
url: /tr/net/aspose.words.tables/table/rightpadding/
---
## Table.RightPadding property

Hücre içeriğinin sağına eklenecek alan miktarını (puan cinsinden) alır veya ayarlar.

```csharp
public double RightPadding { get; set; }
```

### Örnekler

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
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


