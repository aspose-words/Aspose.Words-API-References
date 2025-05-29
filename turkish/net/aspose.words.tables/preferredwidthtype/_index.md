---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: .NET için Aspose.Words
description: Aspose.Words.Tables.PreferredWidthType enum'unu keşfedin. Hassas belge biçimlendirmesi için tablo ve hücre genişliği ölçümlerini kolayca tanımlayın.
type: docs
weight: 7150
url: /tr/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Bir tablonun veya hücrenin tercih edilen genişliği için ölçüm birimini belirtir.

```csharp
public enum PreferredWidthType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `1` | Tercih edilen genişlik belirtilmemiştir. Tablonun veya hücrenin gerçek genişliği, açık genişlik kullanılarak belirtilir veya tablo görüntülendiğinde tablo otomatik uyum ayarına bağlı olarak tablo düzeni algoritması tarafından otomatik olarak belirlenir. |
| Percent | `2` | Belirtilen bir yüzdeyi kullanarak geçerli öğe genişliğini ölçün. |
| Points | `3` | Belirtilen sayıda noktayı (1/72 inç) kullanarak geçerli öğenin genişliğini ölçün. |

## Örnekler

Bir tablo hücresinin tercih edilen genişlik türünün ve değerinin nasıl doğrulanacağını gösterir.

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
