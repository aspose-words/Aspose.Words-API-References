---
title: PreferredWidth.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words for .NET
description: PreferredWidth ToString yöntem. Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.tables/preferredwidth/tostring/
---
## PreferredWidth.ToString method

Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür.

```csharp
public override string ToString()
```

## Örnekler

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
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
