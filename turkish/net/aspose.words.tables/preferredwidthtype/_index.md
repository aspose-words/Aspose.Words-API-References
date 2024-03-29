---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.PreferredWidthType Sıralama. Bir tablo veya hücrenin tercih edilen genişliği için ölçü birimini belirtir C#'da.
type: docs
weight: 6300
url: /tr/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Bir tablo veya hücrenin tercih edilen genişliği için ölçü birimini belirtir.

```csharp
public enum PreferredWidthType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `1` | Tercih edilen genişlik belirtilmemiş. Tablonun veya hücrenin gerçek genişliği ya açık genişlik kullanılarak belirtilir ya da tablo otomatik sığdırma ayarına bağlı olarak tablo görüntülendiğinde tablo düzeni algoritması tarafından otomatik olarak belirlenir. |
| Percent | `2` | Belirtilen yüzdeyi kullanarak geçerli öğe genişliğini ölçün. |
| Points | `3` | Belirtilen sayıda noktayı (1/72 inç) kullanarak geçerli öğe genişliğini ölçün. |

## Örnekler

Bir tablo hücresinin tercih edilen genişlik tipinin ve değerinin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Ayrıca bakınız

* class [PreferredWidth](../preferredwidth/)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
