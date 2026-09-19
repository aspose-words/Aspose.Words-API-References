---
title: "Aspose::Words::NodeChangingArgs classe"
linktitle: "NodeChangingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NodeChangingArgs classe. Fornisce dati per i metodi dell'interfaccia INodeChangingCallback. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words/nodechangingargs/
---
## NodeChangingArgs class


Fornisce dati per i metodi dell'interfaccia [INodeChangingCallback](../inodechangingcallback/). Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeChangingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Action](./get_action/)() const | Ottiene un valore che indica quale tipo di evento di modifica del nodo si sta verificando. |
| [get_NewParent](./get_newparent/)() const | Ottiene il genitore del nodo che sarà impostato al completamento dell'operazione. |
| [get_Node](./get_node/)() const | Ottiene il [Node](./get_node/) che viene aggiunto o rimosso. |
| [get_OldParent](./get_oldparent/)() const | Ottiene il genitore del nodo prima dell'inizio dell'operazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
