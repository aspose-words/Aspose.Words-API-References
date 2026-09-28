---
title: "Aspose::Words::Document::Clone метод"
linktitle: "Клонировать"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::Clone метод. Выполняет глубокое копирование Document в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/document/clone/
---
## Document::Clone method


Выполняет глубокое копирование [Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

Клонированный документ.

## Примеры



Показывает, как выполнить глубокое клонирование документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Клонирование создаст новый документ с тем же содержимым, что и оригинал,
// но с уникальной копией каждого узла оригинального документа.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## См. также

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
