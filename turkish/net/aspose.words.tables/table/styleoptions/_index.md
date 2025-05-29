---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: .NET için Aspose.Words
description: Tablonuzun görünümünü esnek bit bayraklarıyla özelleştirmek için Table StyleOptions özelliğini keşfedin. Tablonuzun stilini zahmetsizce geliştirin!
type: docs
weight: 300
url: /tr/net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

Bu tabloya bir tablo stilinin nasıl uygulanacağını belirten bit bayraklarını alır veya ayarlar.

```csharp
public TableStyleOptions StyleOptions { get; set; }
```

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

* enum [TableStyleOptions](../../tablestyleoptions/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
