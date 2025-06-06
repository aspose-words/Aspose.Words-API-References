---
title: TableStyle.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: .NET için Aspose.Words
description: Tablolarınızdaki hücre hizalamasını zahmetsizce kontrol etmek, okunabilirliği ve sunumu geliştirmek için TableStyle VerticalAlignment özelliğini keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words/tablestyle/verticalalignment/
---
## TableStyle.VerticalAlignment property

Hücreler için dikey hizalamayı belirtir.

```csharp
public CellVerticalAlignment VerticalAlignment { get; set; }
```

## Notlar

Varsayılan değer:Top .

## Örnekler

Tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Bir tablonun stil özelliklerini ayarlamak, tablonun kendi özelliklerini etkileyebilir.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Ayrıca bakınız

* enum [CellVerticalAlignment](../../../aspose.words.tables/cellverticalalignment/)
* class [TableStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
