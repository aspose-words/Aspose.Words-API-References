---
title: "Aspose::Words::SubDocument::get_NodeType método"
linktitle: "get_NodeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::SubDocument::get_NodeType método. Devuelve SubDocument en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Devuelve [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Ejemplos



Muestra cómo acceder al subdocumento de un documento maestro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Este nodo sirve como referencia a un documento externo, y su contenido no puede ser accedido.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## Ver también

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
