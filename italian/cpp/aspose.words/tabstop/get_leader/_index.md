---
title: "Aspose::Words::TabStop::get_Leader metodo"
linktitle: "get_Leader"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStop::get_Leader metodo. Ottiene o imposta il tipo della linea leader visualizzata sotto il carattere di tabulazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/tabstop/get_leader/
---
## TabStop::get_Leader method


Ottiene o imposta il tipo della linea guida visualizzata sotto il carattere di tabulazione.

```cpp
Aspose::Words::TabLeader Aspose::Words::TabStop::get_Leader() const
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

* Enum [TabLeader](../../tableader/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
