---
title: "Aspose::Words::DocumentBuilder::DeleteRow yöntemi"
linktitle: "DeleteRow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::DeleteRow yöntemi. C++'da bir tablodan satır siler."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Bir tablodan bir satırı siler.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableIndex | int32_t | Tablonun indeksi. |
| rowIndex | int32_t | Tablodaki satırın indeksi. |

### ReturnValue

Az önce kaldırılan satır düğümü.
## Açıklamalar


Eğer imleç silinen satırın içinde ise, imleç bir sonraki satıra ya da tablonun sonrasındaki bir sonraki paragrafına taşınır.

Eğer yalnızca bir satır içeren bir tablodan bir satır silerseniz, tüm tablo silinir.

İndeks parametreleri için, indeks 0'a eşit veya daha büyük olduğunda, 0'ın ilk öğe olduğu başlangıçtan bir indeks belirtir. İndeks 0'dan küçük olduğunda, -1'in son öğe olduğu sondan bir indeks belirtir.

## Örnekler



Bir tablodan satır nasıl silinir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Belgedeki ilk tablonun ilk satırını sil.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
