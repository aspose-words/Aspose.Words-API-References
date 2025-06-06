---
title: Table.CellSpacing
linktitle: CellSpacing
articleTitle: CellSpacing
second_title: .NET için Aspose.Words
description: Tablonuzun görünümünü ve okunabilirliğini geliştirmek için hücre aralıklarını noktalar halinde kolayca özelleştirmek amacıyla Table CellSpacing özelliğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

Hücreler arasındaki boşluk miktarını (nokta cinsinden) alır veya ayarlar.

```csharp
public double CellSpacing { get; set; }
```

## Örnekler

Bir tabloda tek tek hücreler arasındaki boşluğun nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Hücreler arasındaki boşluğu etkinleştirmek için "AllowCellSpacing" özelliğini "true" olarak ayarlayın
// "CellSpacing" özelliğinin değerine eşit büyüklükte, noktalar halinde.
// Hücre aralığını devre dışı bırakmak için "AllowCellSpacing" özelliğini "false" olarak ayarlayın
// ve "CellSpacing" özelliğinin değerini yoksay.
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// "CellSpacing" özelliğinin ayarlanması hücre aralığının otomatik olarak etkinleştirilmesini sağlayacaktır.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

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

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
