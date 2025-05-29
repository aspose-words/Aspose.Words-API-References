---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: .NET için Aspose.Words
description: Table LeftPadding özelliğini keşfedin, gelişmiş düzen kontrolü ve iyileştirilmiş tasarım esnekliği için hücre içeriği aralığını noktalar halinde kolayca ayarlayın.
type: docs
weight: 200
url: /tr/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Hücrelerin içeriklerinin soluna eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar.

```csharp
public double LeftPadding { get; set; }
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

 // Tablodaki her hücre için, hücre içeriği ile her bir kenarlık arasındaki mesafeyi ayarlayın.
// Bu tablo metni sararak minimum dolgu mesafesini koruyacaktır.
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
