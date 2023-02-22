---
title: Table.AutoFit
second_title: Aspose.Words for .NET API Referansı
description: Table yöntem. Belirtilen otomatik sığdırma davranışına göre tabloyu ve hücreleri yeniden boyutlandırır.
type: docs
weight: 360
url: /tr/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Belirtilen otomatik sığdırma davranışına göre tabloyu ve hücreleri yeniden boyutlandırır.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| behavior | AutoFitBehavior | Tabloya otomatik olarak nasıl sığdırılacağını belirtir. |

### Notlar

Bu yöntem, Microsoft Word'deki bir tablo için Otomatik Sığdır menüsünde bulunan komutları taklit eder. Mevcut komutlar "İçeriğe Otomatik Sığdır", "Pencereye Otomatik Sığdır" ve "Sabit Sütun Genişliği"dir. Microsoft Word 'de bu komutlar ilgili tablo özelliklerini ayarlar ve ardından tablo düzenini günceller ve Aspose.Words aynısını sizin için yapar.

### Örnekler

Bir stil uygularken yeni bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Herhangi bir tablo biçimlendirmesini ayarlamadan önce en az bir satır eklemeliyiz.
builder.InsertCell();

// Stil tanımlayıcısına göre kullanılan tablo stilini ayarlayın.
// .doc biçiminde kaydederken tüm tablo stillerinin kullanılamayacağını unutmayın.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Tahminlere dayalı olarak stili kısmen tablonun özelliklerine uygulayın, ardından tabloyu oluşturun.
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
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


