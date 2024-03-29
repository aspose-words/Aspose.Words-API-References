---
title: TableStyle.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words for .NET
description: TableStyle LeftIndent mülk. Bir tablonun sol girintisini temsil eden değeri alır veya ayarlar C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

Bir tablonun sol girintisini temsil eden değeri alır veya ayarlar.

```csharp
public double LeftIndent { get; set; }
```

## Örnekler

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

* class [TableStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
