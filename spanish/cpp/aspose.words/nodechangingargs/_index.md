---
title: "Aspose::Words::NodeChangingArgs clase"
linktitle: "NodeChangingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::NodeChangingArgs clase. Proporciona datos para los métodos de la interfaz INodeChangingCallback. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words/nodechangingargs/
---
## NodeChangingArgs class


Proporciona datos para los métodos de la interfaz [INodeChangingCallback](../inodechangingcallback/). Para obtener más información, visite el artículo de documentación del [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeChangingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Action](./get_action/)() const | Obtiene un valor que indica qué tipo de evento de cambio de nodo está ocurriendo. |
| [get_NewParent](./get_newparent/)() const | Obtiene el nodo padre que se establecerá después de que la operación se complete. |
| [get_Node](./get_node/)() const | Obtiene el [Node](./get_node/) que se está agregando o eliminando. |
| [get_OldParent](./get_oldparent/)() const | Obtiene el nodo padre antes de que comenzara la operación. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
