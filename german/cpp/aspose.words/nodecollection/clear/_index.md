---
title: "Aspose::Words::NodeCollection::Clear Methode"
linktitle: "Clear"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeCollection::Clear Methode. Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Beispiele



Zeigt, wie man alle Abschnitte aus einem Dokument entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Dieses Dokument hat einen Abschnitt mit einigen untergeordneten Knoten, die den gesamten Inhalt des Dokuments enthalten und anzeigen.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Leeren Sie die Sammlung der Abschnitte, wodurch alle Kinder des Dokuments entfernt werden.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## Siehe auch

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
