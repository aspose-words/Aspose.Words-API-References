---
title: "Aspose::Words::DocumentBuilder::MoveToSection yöntemi"
linktitle: "MoveToSection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToSection yöntemi. C++'ta belirtilen bir bölümde gövdenin başlangıcına imleci taşır."
type: docs
weight: 60000
url: /tr/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


İmleci belirtilen bölümdeki gövdenin başına taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionIndex | int32_t | Taşınacak bölümün indeksi. |
## Açıklamalar


*sectionIndex* 0'a eşit veya büyük olduğunda, 0'ın ilk bölüm olduğu belgede baştan bir indeks belirtir. *sectionIndex* 0'dan küçük olduğunda, -1'in son bölüm olduğu belgede sondan bir indeks belirtir.

İmleç, belirtilen bölümün [Body](../../body/) içindeki ilk paragrafına taşınır.

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
