---
title: PreferredWidth.FromPoints
linktitle: FromPoints
articleTitle: FromPoints
second_title: .NET için Aspose.Words
description: Tasarım hassasiyetinizi ve verimliliğinizi artırmak için noktalarla tanımlanmış bir genişliğe sahip yeni bir örnek oluşturmak üzere PreferredWidth FromPoints yöntemini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

Belirli sayıda nokta kullanılarak belirtilen tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi.

```csharp
public static PreferredWidth FromPoints(double points)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Değer 0 ile 22 inç (22 * 72 puan) arasında olmalıdır. |

## Örnekler

Bir hücre için tercih edilen genişliği belirlerken birim dönüştürme araçlarının nasıl kullanılacağını gösterir.

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
// 1 - Noktalara dayalı olarak mutlak bir tercih edilen genişlik ayarlayın:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Tablonun genişliğinin yüzdesine göre tercih edilen göreceli genişliği ayarlayın:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Tercih edilen genişliği belirtilmeyen bir hücre kalan kullanılabilir alanı kaplayacaktır.
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
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
