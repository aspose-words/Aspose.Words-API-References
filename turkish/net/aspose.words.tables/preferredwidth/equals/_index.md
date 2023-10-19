---
title: PreferredWidth.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words for .NET
description: PreferredWidth Equals yöntem. Belirtilenin olup olmadığını belirlerPreferredWidth şimdiki değere eşittirPreferredWidth  C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.tables/preferredwidth/equals/
---
## Equals(*[PreferredWidth](../)*) {#equals}

Belirtilenin olup olmadığını belirler[`PreferredWidth`](../) şimdiki değere eşittir[`PreferredWidth`](../) .

```csharp
public bool Equals(PreferredWidth other)
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

---

## Equals(*object*) {#equals_1}

Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler.

```csharp
public override bool Equals(object obj)
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
