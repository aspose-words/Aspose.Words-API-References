---
title: TableStyle.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: .NET için Aspose.Words
description: Tablonuzun düzenini zahmetsizce özelleştirmek ve profesyonel bir görünüm için görsel çekiciliği artırmak amacıyla TableStyle Alignment özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/tablestyle/alignment/
---
## TableStyle.Alignment property

Tablo stili için hizalamayı belirtir.

```csharp
public TableAlignment Alignment { get; set; }
```

## Notlar

Varsayılan değer:Left .

## Örnekler

Bir tablonun konumunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda bir tabloyu yatay olarak hizalamanın iki yolu bulunmaktadır.
// 1 - Sayfanın ortasına gibi bir konuma hizalamak için "Hizalama" özelliğini kullanın:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Bir tablo ekleyelim ve oluşturduğumuz stili ona uygulayalım.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Sayfanın sol kenarından girintiyi belirtmek için "LeftIndent"i kullanın:
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### Ayrıca bakınız

* enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* class [TableStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
