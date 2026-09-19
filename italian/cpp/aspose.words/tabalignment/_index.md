---
title: "Aspose::Words::TabAlignment enum"
linktitle: "TabAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabAlignment enum. Specifica l'allineamento/tipo di una tabulazione in C++."
type: docs
weight: 120000
url: /it/cpp/aspose.words/tabalignment/
---
## TabAlignment enum


Specifica l'allineamento/tipo di una tabulazione.

```cpp
enum class TabAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sinistra | 0 | Allinea a sinistra il testo dopo la tabulazione. |
| Centro | 1 | Centra il testo attorno alla tabulazione. |
| Destra | 2 | Allinea a destra il testo alla tabulazione. |
| Decimale | 3 | Allinea il testo al punto decimale. |
| Barra | 4 | Disegna una barra verticale nella posizione della tabulazione. |
| Elenco | 6 | La tabulazione è un delimitatore tra il numero/punto elenco e il testo in un elemento di elenco. |
| Cancella | 7 | Cancella qualsiasi tabulazione in questa posizione. |


## Esempi



Mostra come impostare tabulazioni personalizzate per un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Se siamo in un paragrafo senza tabulazioni in questa raccolta,
// il cursore salterà di 36 punti ogni volta che premiamo il tasto Tab in Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Possiamo aggiungere tabulazioni personalizzate in Microsoft Word se abilitiamo il righello tramite la scheda "View".
// Ogni unità su questo righello corrisponde a due tabulazioni predefinite, cioè 72 punti.
// Possiamo aggiungere tabulazioni personalizzate programmaticamente in questo modo.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Possiamo vedere queste tabulazioni in Microsoft Word abilitando il righello tramite "View" -> "Show" -> "Ruler".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Qualsiasi carattere di tabulazione che aggiungiamo utilizzerà le tabulazioni sul righello e potrebbe,
// a seconda del valore del leader di tabulazione, lasciare una linea tra la partenza e la destinazione della tabulazione.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
