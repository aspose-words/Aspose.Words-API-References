---
title: "Aspose::Words::Style::get_StyleIdentifier metodo"
linktitle: "get_StyleIdentifier"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Style::get_StyleIdentifier metodo. Ottiene l'identificatore di stile indipendente dalla locale per uno stile predefinito in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words/style/get_styleidentifier/
---
## Style::get_StyleIdentifier method


Ottiene l'identificatore di stile indipendente dalla locale per uno stile predefinito.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Style::get_StyleIdentifier() const
```

## Note


Per gli stili definiti dall'utente (personalizzati), questa proprietà restituisce [User](../../styleidentifier/).

## Esempi



Mostra come modificare la posizione della tab stop destra nei paragrafi correlati al TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Itera attraverso tutti i paragrafi con stili basati sui risultati del TOC; questo è qualsiasi stile compreso tra TOC e TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Ottieni la prima tab usata in questo paragrafo, dovrebbe essere la tab usata per allineare i numeri di pagina.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Sostituisci la prima tab predefinita con una tab stop personalizzata.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Vedi anche

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
