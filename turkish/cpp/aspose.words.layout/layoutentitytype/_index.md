---
title: "Aspose::Words::Layout::LayoutEntityType enum"
linktitle: "LayoutEntityType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutEntityType enum. C++'deki düzen varlıklarının türleri."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Düzen varlıklarının türleri.

```cpp
enum class LayoutEntityType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | n/a | Varsayılan değer. |
| Page | n/a | Bir belgenin sayfasını temsil eder. Sayfa, [Column](./), [HeaderFooter](./) ve [Comment](./) alt varlıklara sahip olabilir. |
| Column | n/a | Bir sayfadaki metin sütununu temsil eder. Sütun, [Cell](./) ile aynı alt varlıklara sahip olabilir, ayrıca [Footnote](./), [Endnote](./) ve [NoteSeparator](./) varlıklarını da içerir. |
| Row | n/a | Bir tablo satırını temsil eder. Satır, alt varlık olarak [Cell](./) içerebilir. |
| Cell | n/a | Bir tablo hücresini temsil eder. Hücre, [Line](./) ve [Row](./) alt varlıklara sahip olabilir. |
| Line | n/a | Metin karakterleri ve satır içi nesnelerden oluşan bir satırı temsil eder. Satır, [Span](./) alt varlıklara sahip olabilir. |
| Span | n/a | Bir satırda bir veya daha fazla karakteri temsil eder. Bu, alan başlangıç/bitiş işaretçileri, yer imleri ve yorumlar gibi özel karakterleri içerir. Span'in alt varlıkları olamaz. |
| Footnote | n/a | Dipnot içeriği için yer tutucuyu temsil eder. Footnote, [Note](./) alt varlıklara sahip olabilir. |
| Endnote | n/a | Son not içeriği için yer tutucuyu temsil eder. Endnote, [Note](./) alt varlıklara sahip olabilir. |
| Note | n/a | Not içeriği için yer tutucuyu temsil eder. Note, [Line](./) ve [Row](./) alt varlıklara sahip olabilir. |
| HeaderFooter | n/a | Bir sayfadaki üstbilgi/altbilgi içeriği için yer tutucuyu temsil eder. [HeaderFooter](../../aspose.words/headerfooter/) [Line](./) ve [Row](./) alt varlıklara sahip olabilir. |
| TextBox | n/a | Bir şekil içindeki metin alanını temsil eder. Textbox, [Line](./) ve [Row](./) alt varlıklara sahip olabilir. |
| Comment | n/a | Yorum içeriği için yer tutucuyu temsil eder. [Comment](../../aspose.words/comment/) [Line](./) ve [Row](./) alt varlıklara sahip olabilir. |
| NoteSeparator | n/a | Dipnot/son not ayırıcıyı temsil eder. NoteSeparator, [Line](./) ve [Row](./) alt varlıklara sahip olabilir. |

## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
