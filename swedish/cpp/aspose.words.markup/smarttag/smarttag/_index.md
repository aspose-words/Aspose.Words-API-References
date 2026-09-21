---
title: "Aspose::Words::Markup::SmartTag::SmartTag konstruktor"
linktitle: "SmartTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SmartTag::SmartTag konstruktor. Initierar en ny instans av SmartTag-klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Initierar en ny instans av [SmartTag](../)-klassen.

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
## Anmärkningar


När du skapar en ny nod måste du ange ett dokument som noden tillhör. En nod kan inte existera utan ett dokument eftersom den är beroende av dokumentomfattande strukturer såsom listor och format. Även om en nod alltid tillhör ett dokument, kan den vara en del av dokumentträdet eller inte.

När en nod skapas tillhör den ett dokument, men är ännu inte en del av dokumentträdet och [ParentNode](../../../aspose.words/node/get_parentnode/) är null. För att infoga en nod i dokumentet, använd [InsertAfter1()</see> eller <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) metoder på föräldranoden.

## Se även

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
