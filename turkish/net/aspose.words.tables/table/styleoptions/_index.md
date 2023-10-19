---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: Aspose.Words for .NET
description: Table StyleOptions mülk. Bir tablo stilinin bu tabloya nasıl uygulanacağını belirten bit bayraklarını alır veya ayarlar C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

Bir tablo stilinin bu tabloya nasıl uygulanacağını belirten bit bayraklarını alır veya ayarlar.

```csharp
public TableStyleOptions StyleOptions { get; set; }
```

## Örnekler

Stil uygularken yeni bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Herhangi bir tablo formatını ayarlamadan önce en az bir satır eklemeliyiz.
builder.InsertCell();

// Kullanılan tablo stilini stil tanımlayıcıya göre ayarlayın.
// .doc formatında kaydederken tüm tablo stillerinin kullanılamayacağını unutmayın.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Stili, yüklemlere dayalı olarak tablonun özelliklerine kısmen uygulayın, ardından tabloyu oluşturun.
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
