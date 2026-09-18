---
title: "Aspose::Words::NodeCollection::RemoveAt Methode"
linktitle: "RemoveAt"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeCollection::RemoveAt Methode. Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Der nullbasierte Index des Knotens. Negative Indizes sind erlaubt und bedeuten den Zugriff vom Ende der Liste aus. Zum Beispiel bedeutet -1 den letzten Knoten, -2 den vorletzten und so weiter. |

## Beispiele



Zeigt, wie man Abschnitte in einem Dokument hinzufügt und entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Löschen Sie den ersten Abschnitt aus dem Dokument.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Fügen Sie eine Kopie des jetzt ersten Abschnitts am Ende des Dokuments an.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Siehe auch

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
