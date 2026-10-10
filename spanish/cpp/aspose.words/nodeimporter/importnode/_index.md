---
title: "Método Aspose::Words::NodeImporter::ImportNode"
linktitle: "ImportNode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeImporter::ImportNode. Importa un nodo de un documento a otro en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Importa un nodo de un documento a otro.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo a importar. |
| isImportChildren | bool | **true** para importar todos los nodos hijos de forma recursiva; de lo contrario, **false**. |

### ReturnValue

El nodo clonado e importado. El nodo pertenece al documento de destino, pero no tiene padre.
## Observaciones


Importar un nodo crea una copia del nodo origen que pertenece al documento de importación. El nodo devuelto no tiene padre. El nodo origen no se altera ni se elimina del documento original.

Antes de que un nodo de otro documento pueda insertarse en este documento, debe importarse. Durante la importación, las propiedades específicas del documento, como referencias a estilos y listas, se traducen del original al documento de importación. Después de que el nodo se haya importado, puede insertarse en el lugar apropiado del documento usando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Si el nodo origen ya pertenece al documento de destino, simplemente se crea una clonación profunda del nodo origen.

## Ver también

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
