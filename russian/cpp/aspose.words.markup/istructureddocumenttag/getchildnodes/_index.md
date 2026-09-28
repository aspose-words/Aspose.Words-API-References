---
title: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method"
linktitle: "GetChildNodes"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method. Возвращает живую коллекцию дочерних узлов, соответствующих указанным типам в C++."
type: docs
weight: 14500
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


Возвращает живую коллекцию дочерних узлов, соответствующих указанным типам.

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
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

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
