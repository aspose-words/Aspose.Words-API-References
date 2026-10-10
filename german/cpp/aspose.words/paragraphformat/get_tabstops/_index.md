---
title: "Aspose::Words::ParagraphFormat::get_TabStops Methode"
linktitle: "get_TabStops"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_TabStops Methode. Gibt die Sammlung der benutzerdefinierten Tabstopps zurück, die für dieses Objekt in C++ definiert sind."
type: docs
weight: 40000
url: /de/cpp/aspose.words/paragraphformat/get_tabstops/
---
## ParagraphFormat::get_TabStops method


Liest die Sammlung benutzerdefinierter Tabulatoren, die für dieses Objekt definiert sind.

```cpp
System::SharedPtr<Aspose::Words::TabStopCollection> Aspose::Words::ParagraphFormat::get_TabStops()
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

* Class [TabStopCollection](../../tabstopcollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
