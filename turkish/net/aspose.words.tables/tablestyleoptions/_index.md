---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: .NET için Aspose.Words
description: Esnek tablo stili için Aspose.Words.Tables.TableStyleOptions enum'unu keşfedin. Özelleştirilebilir tablo stilleriyle belge tasarımınızı bugün geliştirin!
type: docs
weight: 7220
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
| FirstRow | `20` | İlk satır koşullu biçimlendirmesini uygula. |
| LastRow | `40` | Son satıra koşullu biçimlendirme uygula. |
| FirstColumn | `80` | İlk sütuna koşullu biçimlendirme uygula. |
| LastColumn | `100` | Son sütuna koşullu biçimlendirme uygula. |
| RowBands | `200` | Satır bantlama koşullu biçimlendirmesini uygula. |
| ColumnBands | `400` | Sütun bantlama koşullu biçimlendirmesini uygula. |
| Default2003 | `600` | Satır ve sütun bantlaması uygulanır. Bu, DOC, WML ve RTF gibi eski biçimler için Microsoft Word varsayılanıdır. |
| Default | `2A0` | Bu Microsoft Word varsayılanlarıdır. |

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

* property [StyleOptions](../table/styleoptions/)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
