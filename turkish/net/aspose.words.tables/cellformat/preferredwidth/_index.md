---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: .NET için Aspose.Words
description: E-tablolarınızda optimum düzen ve tasarım için hücre genişliklerini kolayca özelleştirmek üzere CellFormat PreferredWidth özelliğini keşfedin. Veri sunumunuzu geliştirin!
type: docs
weight: 80
url: /tr/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Hücrenin tercih edilen genişliğini döndürür veya ayarlar.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Notlar

Tercih edilen genişlik (tablonun Otomatik Uyum seçeneğiyle birlikte) hücrenin gerçek genişliğinin tablo düzeni algoritması tarafından nasıl hesaplandığını belirler. Tablo düzeni, belgeyi kaydederken Aspose.Words tarafından veya belgeyi görüntülerken Microsoft Word tarafından gerçekleştirilebilir.

Tercih edilen genişlik puan veya yüzde olarak belirtilebilir. Tercih edilen width "auto" olarak da belirtilebilir, bu da tercih edilen bir genişliğin belirtilmediği anlamına gelir.

Varsayılan değer:[`Auto`](../../preferredwidth/auto/).

## Örnekler

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
