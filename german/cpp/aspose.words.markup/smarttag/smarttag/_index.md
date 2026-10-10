---
title: "Aspose::Words::Markup::SmartTag::SmartTag Konstruktor"
linktitle: "SmartTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::SmartTag::SmartTag Konstruktor. Initialisiert eine neue Instanz der SmartTag-Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Initialisiert eine neue Instanz der [SmartTag](../)-Klasse.

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
## Hinweise


Wenn Sie einen neuen Knoten erstellen, müssen Sie ein Dokument angeben, zu dem der Knoten gehört. Ein Knoten kann nicht ohne ein Dokument existieren, da er von dokumentweiten Strukturen wie Listen und Formatvorlagen abhängt. Obwohl ein Knoten immer zu einem Dokument gehört, kann er Teil des Dokumentbaums sein oder auch nicht.

Wenn ein Knoten erstellt wird, gehört er zu einem Dokument, ist aber noch nicht Teil des Dokumentbaums und [ParentNode](../../../aspose.words/node/get_parentnode/) ist null. Um einen Knoten in das Dokument einzufügen, verwenden Sie die [InsertAfter1()</see> oder <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) Methoden am übergeordneten Knoten.

## Siehe auch

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
