---
title: "Aspose::Words::TabStop::get_Alignment Methode"
linktitle: "get_Alignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStop::get_Alignment-Methode. Gibt die Ausrichtung des Textes an diesem Tabstopp zurück oder legt sie fest in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/tabstop/get_alignment/
---
## TabStop::get_Alignment method


Liest oder legt die Ausrichtung des Textes an diesem Tabstopp fest.

```cpp
Aspose::Words::TabAlignment Aspose::Words::TabStop::get_Alignment() const
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

* Enum [TabAlignment](../../tabalignment/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
