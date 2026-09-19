---
title: "Metodo Aspose::Words::NodeImporter::ImportNode"
linktitle: "ImportNode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::NodeImporter::ImportNode. Importa un nodo da un documento all'altro in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Importa un nodo da un documento a un altro.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da importare. |
| isImportChildren | bool | **true** per importare tutti i nodi figlio ricorsivamente; altrimenti, **false**. |

### ReturnValue

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha genitore.
## Note


L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento di destinazione. Il nodo restituito non ha genitore. Il nodo sorgente non viene modificato né rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili e elenchi vengono tradotte dall'originale al documento di destinazione. Dopo che il nodo è stato importato, può essere inserito nel punto appropriato del documento utilizzando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creata una clonazione profonda del nodo sorgente.

## Vedi anche

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
