---
title: "Aspose::Words::ParagraphCollection::ToArray метод"
linktitle: "ToArray"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphCollection::ToArray. Копирует все абзацы из коллекции в новый массив абзацев в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Копирует все абзацы из коллекции в новый массив абзацев.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

Массив абзацев.

## Примеры



Показывает, как создать массив из [NodeCollection](../../nodecollection/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Показывает, как использовать \"hot remove\" для удаления узла во время перечисления.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Удалить узел из коллекции в середине перечисления.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## См. также

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
