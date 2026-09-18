---
title: "Aspose::Words::TabStopCollection::RemoveByIndex-Methode"
linktitle: "RemoveByIndex"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection::RemoveByIndex-Methode. Entfernt einen Tabstopp am angegebenen Index aus der Sammlung in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


Entfernt einen Tabulator am angegebenen Index aus der Sammlung.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Sammlung der Tabstopps. |

## Beispiele



Zeigt, wie man einen Tabstopp in einem Dokument anhand seines Index auswählt und entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// Entferne den ersten Tabstopp.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## Siehe auch

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
