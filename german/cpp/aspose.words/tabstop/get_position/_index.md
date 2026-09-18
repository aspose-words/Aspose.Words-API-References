---
title: "Aspose::Words::TabStop::get_Position-Methode"
linktitle: "get_Position"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStop::get_Position-Methode. Gibt die Position des Tabstopps in Punkten in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words/tabstop/get_position/
---
## TabStop::get_Position method


Liest die Position des Tabstopps in Punkten.

```cpp
double Aspose::Words::TabStop::get_Position()
```


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

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
