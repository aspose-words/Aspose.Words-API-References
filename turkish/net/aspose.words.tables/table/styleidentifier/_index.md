---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words for .NET
description: Table StyleIdentifier mülk. Bu tabloya uygulanan tablo stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar C#'da.
type: docs
weight: 280
url: /tr/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Bu tabloya uygulanan tablo stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
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

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
