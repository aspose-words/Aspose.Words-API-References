---
title: "Aspose::Words::NodeList::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeList::idx_get Methode. Ruft einen Knoten am angegebenen Index in C++ ab."
type: docs
weight: 6000
url: /de/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Ruft einen Knoten am angegebenen Index ab.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Knotenliste. |
## Hinweise


Der Index ist nullbasiert.

Negative Indizes sind erlaubt und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer als oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer ist als die Anzahl der Elemente in der Liste, gibt dies eine Nullreferenz zurück.

## Siehe auch

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
