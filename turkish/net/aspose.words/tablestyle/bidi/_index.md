---
title: Bidi
second_title: Aspose.Words for .NET API Referansı
description: Bunun sağdan sola tablo için bir stil olup olmadığını alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words/tablestyle/bidi/
---
## TableStyle.Bidi property

Bunun sağdan sola tablo için bir stil olup olmadığını alır veya ayarlar.

```csharp
public bool Bidi { get; set; }
```

### Notlar

Ne zaman **doğru**, satırlardaki hücreler sağdan sola yerleştirilir.

Varsayılan değer **yanlış**.

### Örnekler

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

// Bir tablonun stil özelliklerini ayarlamak, tablonun özelliklerini etkileyebilir.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Ayrıca bakınız

* class [TableStyle](../../tablestyle)
* ad alanı [Aspose.Words](../../tablestyle)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->