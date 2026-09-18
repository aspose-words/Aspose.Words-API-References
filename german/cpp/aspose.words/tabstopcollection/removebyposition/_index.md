---
title: "Aspose::Words::TabStopCollection::RemoveByPosition method"
linktitle: "RemoveByPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection::RemoveByPosition Methode. Entfernt einen Tabstopp an der angegebenen Position aus der Sammlung in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


Entfernt einen Tabulator an der angegebenen Position aus der Sammlung.

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Position | double | Die Position (in Punkten) des zu entfernenden Tabstopps. |

## Beispiele



Zeigt, wie die Position des rechten Tabstopps in TOC‑bezogenen Absätzen geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Durchlaufen Sie alle Absätze mit TOC‑ergebnisbasierten Stilen; das ist jeder Stil zwischen TOC und TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Ermitteln Sie den ersten Tab, der in diesem Absatz verwendet wird; dies sollte der Tab sein, der zum Ausrichten der Seitenzahlen verwendet wird.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Ersetzen Sie den ersten Standard‑Tabstopp durch einen benutzerdefinierten Tabstopp.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Siehe auch

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
