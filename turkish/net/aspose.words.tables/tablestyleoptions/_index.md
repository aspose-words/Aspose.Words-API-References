---
title: Enum TableStyleOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Tables.TableStyleOptions Sıralama. Tablo stilinin bir tabloya nasıl uygulanacağını belirtir.
type: docs
weight: 6070
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
| FirstRow | `20` | İlk satır koşullu biçimlendirmeyi uygula. |
| LastRow | `40` | Son satır koşullu biçimlendirmesini uygula. |
| FirstColumn | `80` | 1 ilk sütun koşullu biçimlendirmesini uygulayın. |
| LastColumn | `100` | Son sütun koşullu biçimlendirmesini uygula. |
| RowBands | `200` | Satır bantlama koşullu biçimlendirmesini uygulayın. |
| ColumnBands | `400` | Sütun bantlama koşullu biçimlendirmesini uygula. |
| Default2003 | `600` | Satır ve sütun bantlaması uygulandı. Bu, DOC, WML ve RTF gibi eski biçimler için Microsoft Word varsayılanıdır. |
| Default | `2A0` | Bu, Microsoft Word varsayılanlarıdır. |

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

* property [StyleOptions](../table/styleoptions/)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)


