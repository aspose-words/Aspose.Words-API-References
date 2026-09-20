---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly метод"
linktitle: "RemoveSelfOnly"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly метод. Удаляет только этот узел SDT, но сохраняет его содержимое внутри дерева документа в C++."
type: docs
weight: 17500
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Удаляет только этот узел SDT, но сохраняет его содержимое в дереве документа.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
```


## Примеры



Показывает, как удалить структурированный тег документа, но сохраняет содержимое внутри.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Эта коллекция предоставляет единый интерфейс для доступа к диапазонным и недиапазонным структурированным тегам.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Здесь мы можем получить дочерние узлы из общего интерфейса диапазонных и недиапазонных структурированных тегов.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## См. также

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
