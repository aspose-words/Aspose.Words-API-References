---
title: PreferredWidth.Auto
second_title: Aspose.Words for .NET API Referansı
description: PreferredWidth alan. Tercih edilen genişlik belirtilmedi değerini temsil eden bir örneği döndürür.
type: docs
weight: 10
url: /tr/net/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth.Auto field

"Tercih edilen genişlik belirtilmedi" değerini temsil eden bir örneği döndürür.

```csharp
public static readonly PreferredWidth Auto;
```

### Örnekler

Tablo hücreleri için tercih edilen genişliğin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// "PreferredWidth" sınıfını tablo hücrelerine uygulamanın iki yolu vardır.
// 1 - Noktalara dayalı olarak tercih edilen mutlak genişliği ayarlayın:
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

// Tercih edilen genişliği belirtilmeyen bir hücre, kullanılabilir alanın geri kalanını kaplayacaktır.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// "PreferredWidth" özelliğinin her konfigürasyonu yeni bir nesne oluşturur.
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


