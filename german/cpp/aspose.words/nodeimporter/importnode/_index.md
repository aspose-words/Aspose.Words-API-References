---
title: "Aspose::Words::NodeImporter::ImportNode-Methode"
linktitle: "ImportNode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeImporter::ImportNode-Methode. Importiert einen Knoten von einem Dokument in ein anderes in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Importiert einen Knoten von einem Dokument in ein anderes.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Der zu importierende Knoten. |
| isImportChildren | bool | **true** um alle untergeordneten Knoten rekursiv zu importieren; andernfalls **false**. |

### ReturnValue

Der geklonte, importierte Knoten. Der Knoten gehört zum Ziel-Dokument, hat aber keinen übergeordneten Knoten.
## Hinweise


Das Importieren eines Knotens erstellt eine Kopie des Quellknotens, die zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen Elternknoten. Der Quellknoten wird nicht verändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss er importiert werden. Während des Imports werden dokumentbezogene Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er an die passende Stelle im Dokument eingefügt werden, indem man [InsertBefore1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertAfter1()](../) verwendet.

Wenn der Quellknoten bereits zum Ziel‑Dokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Siehe auch

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
