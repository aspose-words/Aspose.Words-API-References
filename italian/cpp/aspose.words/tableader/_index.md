---
title: "Aspose::Words::TabLeader enum"
linktitle: "TabLeader"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabLeader enum. Specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione in C++."
type: docs
weight: 121000
url: /it/cpp/aspose.words/tableader/
---
## TabLeader enum


Specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione.

```cpp
enum class TabLeader
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Nessuna linea guida viene visualizzata. |
| Punti | 1 | La linea guida è composta da punti. |
| Trattini | 2 | La linea guida è composta da trattini. |
| Linea | 3 | La linea guida è una singola linea. |
| Spessa | 4 | La linea guida è una singola linea spessa. |
| MiddleDot | 5 | La linea guida è composta da punti centrali. |


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
