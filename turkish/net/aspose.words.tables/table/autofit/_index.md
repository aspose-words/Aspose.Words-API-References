---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: .NET için Aspose.Words
description: Tabloları ve hücreleri en iyi düzen için zahmetsizce yeniden boyutlandırmak için Tablo Otomatik Sığdırma yöntemini keşfedin. Belgenizin sunumunu kolaylıkla geliştirin!
type: docs
weight: 380
url: /tr/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Tabloyu ve hücreleri belirtilen otomatik uyum davranışına göre yeniden boyutlandırır.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| behavior | AutoFitBehavior | Tablonun otomatik olarak nasıl sığdırılacağını belirtir. |

## Notlar

Bu yöntem, Microsoft Word'deki bir tablo için Otomatik Sığdırma menüsünde bulunan komutları taklit eder. Kullanılabilir komutlar "İçeriğe Otomatik Sığdır", "Pencereye Otomatik Sığdır" ve "Sabit Sütun Genişliği"dir. Microsoft Word 'de bu komutlar ilgili tablo özelliklerini ayarlar ve ardından tablo düzenini günceller ve Aspose.Words sizin için aynısını yapar.

## Örnekler

Bir stil uygulanırken yeni bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Herhangi bir tablo biçimlendirmesini ayarlamadan önce en az bir satır eklemeliyiz.
builder.InsertCell();

// Stil tanımlayıcısına göre kullanılan tablo stilini ayarlayın.
// .doc formatına kaydederken tüm tablo stillerinin kullanılamayacağını unutmayın.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Tablonun özelliklerine tahminlere dayalı olarak stili kısmen uygulayın, ardından tabloyu oluşturun.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Ayrıca bakınız

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
