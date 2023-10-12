---
title: TableStyle.Alignment
second_title: Aspose.Words for .NET API Referansı
description: TableStyle mülk. Tablo stilinin hizalamasını belirtir.
type: docs
weight: 10
url: /tr/net/aspose.words/tablestyle/alignment/
---
## TableStyle.Alignment property

Tablo stilinin hizalamasını belirtir.

```csharp
public TableAlignment Alignment { get; set; }
```

### Notlar

Varsayılan değer:Left .

### Örnekler

Bir tablonun konumunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda bir tabloyu yatay olarak hizalamanın iki yolu verilmiştir.
// 1 - Sayfanın merkezi gibi bir konuma hizalamak için "Hizalama" özelliğini kullanın:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Bir tablo ekleyin ve oluşturduğumuz stili ona uygulayın.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Sayfanın sol kenar boşluğundan bir girinti belirtmek için "LeftIndent" seçeneğini kullanın:
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
* ad alanı [Aspose.Words](../../tablestyle/)
* toplantı [Aspose.Words](../../../)


