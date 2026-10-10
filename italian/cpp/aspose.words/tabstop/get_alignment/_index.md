---
title: "Aspose::Words::TabStop::get_Alignment metodo"
linktitle: "get_Alignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStop::get_Alignment metodo. Ottiene o imposta l'allineamento del testo a questa tabulazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/tabstop/get_alignment/
---
## TabStop::get_Alignment method


Ottiene o imposta l'allineamento del testo a questa tab stop.

```cpp
Aspose::Words::TabAlignment Aspose::Words::TabStop::get_Alignment() const
```


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

* Enum [TabAlignment](../../tabalignment/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
