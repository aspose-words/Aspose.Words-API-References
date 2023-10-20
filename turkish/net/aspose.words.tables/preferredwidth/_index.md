---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.PreferredWidth sınıf. Bir tablonun veya hücrenin tercih edilen genişliğini belirtmek için kullanılan bir değeri ve onun ölçü birimini temsil eder C#'da.
type: docs
weight: 6290
url: /tr/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Bir tablonun veya hücrenin tercih edilen genişliğini belirtmek için kullanılan bir değeri ve onun ölçü birimini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Tablolarla Çalışmak](https://docs.aspose.com/words/net/working-with-tables/) dokümantasyon makalesi.

```csharp
public sealed class PreferredWidth
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Tercih edilen bu genişlik değeri için kullanılan ölçü birimini alır. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Tercih edilen genişlik değerini alır. Ölçü birimi belirtilen[`Type`](./type/) özellik. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | Yüzde olarak belirtilen tercih edilen genişliği temsil eden yeni bir örneği döndüren bir oluşturma yöntemi. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | Bir dizi nokta kullanılarak belirtilen tercih edilen genişliği temsil eden yeni bir örneği döndüren bir oluşturma yöntemi. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Belirtilenin olup olmadığını belirler`PreferredWidth` şimdiki değere eşittir`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Bu tür için karma işlevi görevi görür. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür. |

## Alanlar

| İsim | Tanım |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | "Tercih edilen genişlik belirtilmedi" değerini temsil eden bir örneği döndürür. |

## Notlar

Tercih edilen genişlik yüzde, nokta sayısı veya özel bir "yok/otomatik" değer olarak belirtilebilir.

Bu sınıfın örnekleri değişmezdir.

## Örnekler

Bir tablonun sayfa genişliğinin %50'sine otomatik olarak sığacak şekilde nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

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

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
