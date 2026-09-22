---
title: "Aspose::Words::DocumentBuilder::MoveToCell yöntemi"
linktitle: "MoveToCell"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToCell yöntemi. İmleci, C++'ta geçerli bölümdeki bir tablo hücresine taşır."
type: docs
weight: 53000
url: /tr/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


İmleci geçerli bölümdeki bir tablo hücresine taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableIndex | int32_t | Gitmek istediğiniz tablonun indeksi. |
| rowIndex | int32_t | Tablodaki satırın indeksi. |
| columnIndex | int32_t | Tablodaki sütunun indeksi. |
| characterIndex | int32_t | Hücre içindeki karakterin indeksi. Negatif bir değer, hücrenin sonundan bir konum belirtmenizi sağlar. Hücrenin sonuna gitmek için -1 kullanın. |
## Açıklamalar


Gezinti, geçerli bölümün mevcut hikâyesi içinde gerçekleştirilir.

İndeks parametreleri için, indeks 0'a eşit veya daha büyük olduğunda, 0'ın ilk öğe olduğu başlangıçtan bir indeks belirtir. İndeks 0'dan küçük olduğunda, -1'in son öğe olduğu sondan bir indeks belirtir.

## Örnekler



DocumentBuilder'ın imlecini bir tablodaki hücreye nasıl taşıyacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Boş bir 2x2 tablo oluşturun.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Tabloyu EndTable yöntemiyle sonlandırdığımız için,
// DocumentBuilder'ın imleci şu anda tablonun dışındadır.
// Bu imlecin işlevi, Microsoft Word'ün yanıp sönen metin imlecine aynıdır.
// Ayrıca, builder'ın MoveTo yöntemlerini kullanarak belge içinde farklı bir konuma da taşınabilir.
// İmleci tablo içinde belirli bir hücreye geri taşıyabiliriz.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
