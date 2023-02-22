---
title: PreferredWidth.FromPoints
second_title: Aspose.Words for .NET API Referansı
description: PreferredWidth yöntem. Bir dizi nokta kullanılarak belirtilen tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi.
type: docs
weight: 30
url: /tr/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

Bir dizi nokta kullanılarak belirtilen tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi.

```csharp
public static PreferredWidth FromPoints(double points)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Değer 0 - 22 inç (22 * 72 punto) arasında olmalıdır. |

### Örnekler

Bir hücre için tercih edilen genişlik belirtilirken birim dönüştürme araçlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.AreEqual(216.0d, table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value);
```

Tablo hücreleri için tercih edilen genişliğin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// "PreferredWidth" sınıfını tablo hücrelerine uygulamanın iki yolu vardır.
// 1 - Noktalara göre mutlak bir tercih edilen genişlik ayarlayın:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Tablonun genişliğinin yüzdesine göre göreli bir tercih edilen genişlik ayarlayın:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Tercih edilen genişlik belirtilmemiş bir hücre, kullanılabilir alanın geri kalanını alacaktır.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// "PreferredWidth" özelliğinin her yapılandırması yeni bir nesne oluşturur.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Ayrıca bakınız

* class [PreferredWidth](../)
* ad alanı [Aspose.Words.Tables](../../preferredwidth/)
* toplantı [Aspose.Words](../../../)


