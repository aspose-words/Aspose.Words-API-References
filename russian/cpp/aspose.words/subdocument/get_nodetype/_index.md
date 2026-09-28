---
title: "Метод Aspose::Words::SubDocument::get_NodeType"
linktitle: "get_NodeType"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::SubDocument::get_NodeType. Возвращает SubDocument в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Возвращает [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Примеры



Показывает, как получить доступ к поддокументу основного документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Этот узел служит ссылкой на внешний документ, и его содержимое недоступно.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## См. также

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
