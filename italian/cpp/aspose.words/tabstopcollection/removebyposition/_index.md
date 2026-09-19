---
title: "Metodo Aspose::Words::TabStopCollection::RemoveByPosition"
linktitle: "RemoveByPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::TabStopCollection::RemoveByPosition. Rimuove una tabulazione nella posizione specificata dalla collezione in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


Rimuove una tabulazione alla posizione specificata dalla raccolta.

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double | La posizione (in punti) della tabulazione da rimuovere. |

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

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
