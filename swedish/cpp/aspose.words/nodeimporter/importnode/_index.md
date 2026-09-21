---
title: "Aspose::Words::NodeImporter::ImportNode metod"
linktitle: "ImportNode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeImporter::ImportNode metod. Importerar en nod från ett dokument till ett annat i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Importerar en nod från ett dokument till ett annat.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden som ska importeras. |
| isImportChildren | bool | **true** för att importera alla barnnoder rekursivt; annars **false**. |

### ReturnValue

Den klonade, importerade noden. Noden tillhör destinationsdokumentet, men har ingen förälder.
## Anmärkningar


Att importera en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras inte eller tas bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokument‑specifika egenskaper såsom referenser till stilar och listor från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av [InsertBefore1()</see> eller <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djupklon av källnoden.

## Se även

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
