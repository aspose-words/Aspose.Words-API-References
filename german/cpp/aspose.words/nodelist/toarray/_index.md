---
title: "Aspose::Words::NodeList::ToArray Methode"
linktitle: "ToArray"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeList::ToArray Methode. Kopiert alle Knoten aus der Sammlung in ein neues Knoten‑Array in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Kopiert alle Knoten aus der Sammlung in ein neues Knotenarray.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

Ein Array von Knoten.
## Hinweise


Sie sollten keine Knoten hinzufügen/entfernen, während Sie über eine Knotensammlung iterieren, da dies den Iterator ungültig macht und Aktualisierungen für Live-Sammlungen erfordert.

Um während der Iteration Knoten hinzufügen/entfernen zu können, verwenden Sie diese Methode, um Knoten in ein festes Array zu kopieren und dann über das Array zu iterieren.

## Siehe auch

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
