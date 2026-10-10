---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes metodo"
linktitle: "GetChildNodes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes metodo. Restituisce una collezione live di nodi figlio che corrispondono al tipo specificato in C++."
type: docs
weight: 34500
url: /it/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Specifica il tipo di nodi da selezionare. |
| isDeep | bool | **true** per selezionare tutti i nodi figlio ricorsivamente; **false** per selezionare solo tra i figli immediati. |

### ReturnValue

Una collezione live di nodi figlio del tipo specificato.
## Note


La collezione di nodi restituita da questo metodo è sempre live.

Una collezione live è sempre sincronizzata con il documento. Ad esempio, se selezioni tutte le sezioni in un documento e le enumeri attraverso la collezione eliminando le sezioni, la sezione viene rimossa dalla collezione immediatamente quando viene rimossa dal documento.

## Vedi anche

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
