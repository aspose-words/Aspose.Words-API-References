---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.TableStyleOptions Sıralama. Tablo stilinin bir tabloya nasıl uygulanacağını belirtir C#'da.
type: docs
weight: 6370
url: /tr/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Tablo stilinin bir tabloya nasıl uygulanacağını belirtir.

```csharp
[Flags]
public enum TableStyleOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Tablo stili biçimlendirmesi uygulanmadı. |
| FirstRow | `20` | İlk satıra koşullu biçimlendirmeyi uygula. |
| LastRow | `40` | Son satıra koşullu biçimlendirmeyi uygula. |
| FirstColumn | `80` | İlk sütuna 1 koşullu biçimlendirme uygulayın. |
| LastColumn | `100` | Son sütuna koşullu biçimlendirmeyi uygula. |
| RowBands | `200` | Satır bantlama koşullu biçimlendirmesini uygulayın. |
| ColumnBands | `400` | Sütun bantlama koşullu biçimlendirmesini uygulayın. |
| Default2003 | `600` | Satır ve sütun bantlaması uygulandı. Bu, DOC, WML ve RTF gibi eski formatlar için Microsoft Word'ün varsayılanıdır. |
| Default | `2A0` | Bu, Microsoft Word varsayılanlarıdır. |

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

* property [StyleOptions](../table/styleoptions/)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
