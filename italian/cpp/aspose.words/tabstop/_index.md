---
title: "Aspose::Words::TabStop class"
linktitle: "TabStop"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStop class. Rappresenta una singola tabulazione personalizzata. L'oggetto TabStop è un membro della raccolta TabStopCollection. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 68000
url: /it/cpp/aspose.words/tabstop/
---
## TabStop class


Rappresenta una singola tabulazione personalizzata. L'oggetto [TabStop](./) è un membro della raccolta [TabStopCollection](../tabstopcollection/). Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Confronta con il [TabStop](./) specificato. |
| [get_Alignment](./get_alignment/)() const | Ottiene o imposta l'allineamento del testo a questa tab stop. |
| [get_IsClear](./get_isclear/)() | Restituisce **true** se questa tab stop elimina eventuali tab stop esistenti in questa posizione. |
| [get_Leader](./get_leader/)() const | Ottiene o imposta il tipo della linea guida visualizzata sotto il carattere di tabulazione. |
| [get_Position](./get_position/)() | Ottiene la posizione della tab stop in punti. |
| [GetHashCode](./gethashcode/)() const override | Calcola il codice hash per questo oggetto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Impostatore per [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Impostatore per [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Inizializza una nuova istanza di questa classe. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Inizializza una nuova istanza di questa classe. |
| static [Type](./type/)() |  |
## Note


Normalmente, una tab stop specifica una posizione in cui è presente una tab stop. Tuttavia, poiché le tab stop possono essere ereditate dagli stili genitore, potrebbe essere necessario che l'oggetto figlio definisca esplicitamente che non esiste alcuna tab stop in una data posizione. Per cancellare una tab stop ereditata in una data posizione, crea un oggetto [TabStop](./) e imposta [Alignment](./get_alignment/) su [Clear](../tabalignment/).

Per ulteriori informazioni, vedere [TabStopCollection](../tabstopcollection/).

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
