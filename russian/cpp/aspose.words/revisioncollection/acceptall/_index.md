---
title: "Aspose::Words::RevisionCollection::AcceptAll метод"
linktitle: "AcceptAll"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::RevisionCollection::AcceptAll метод. Принимает все ревизии в этой коллекции в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Принимает все изменения в этой коллекции.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Примеры



Показывает, как сравнивать документы.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Сравнение документов с правками вызовет исключение.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// После сравнения оригинальный документ получит новую правку
// для каждого элемента, отличающегося в отредактированном документе.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Принятие этих правок преобразует оригинальный документ в отредактированный документ.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## См. также

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
