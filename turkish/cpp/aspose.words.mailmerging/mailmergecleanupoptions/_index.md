---
title: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum"
linktitle: "MailMergeCleanupOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum. Posta birleştirme sırasında C++'ta hangi öğelerin kaldırılacağını belirleyen seçenekleri tanımlar."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirleyen seçenekleri belirtir.

```cpp
enum class MailMergeCleanupOptions
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Varsayılan bir değeri belirtir. |
| RemoveEmptyParagraphs | 1 | Belirtilen paragrafın, veri içermeyen posta birleştirme alanları içeriyorsa belgeden kaldırılıp kaldırılmayacağını belirtir. Bu seçenek ayarlandığında, aksi takdirde boş olan bölge başlangıç ve bitiş birleştirme alanlarını içeren paragraflar da kaldırılır. |
| RemoveUnusedRegions | 2 | Kullanılmayan posta birleştirme bölgelerinin belgelerden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveUnusedFields | 4 | Kullanılmayan birleştirme alanlarının belgelerden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveContainingFields | 8 | İçinde birleştirme alanları (örneğin IF'ler) bulunan alanların, iç içe birleştirme alanları kaldırıldığında belgelerden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveStaticFields | 16 | Belgenin statik alanlardan temizlenip temizlenmeyeceğini belirtir. Statik alanlar, belge değiştiğinde sonuçları aynı kalan alanlardır. [Fields](../../aspose.words.fields/), sonuçlarını bir belgede saklamayan ve anlık olarak hesaplanan (örneğin [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/) vb.) alanlar statik olarak kabul edilmez. |
| RemoveEmptyTableRows | 32 | Posta birleştirme bölgeleri içeren boş satırların belgelerden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveEmptyTables | 64 | Belgeden, [RemoveUnusedRegions](./) veya [RemoveEmptyTableRows](./) seçeneği kullanılarak kaldırılan posta birleştirme bölgelerini içeren tabloların kaldırılıp kaldırılmayacağını belirtir. |

## Ayrıca Bakınız

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
