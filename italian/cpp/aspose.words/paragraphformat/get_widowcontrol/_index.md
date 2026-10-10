---
title: "Metodo Aspose::Words::ParagraphFormat::get_WidowControl"
linktitle: "get_WidowControl"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_WidowControl. True se le prime e le ultime righe del paragrafo devono rimanere nella stessa pagina del resto del paragrafo in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


Vero se la prima e l'ultima riga del paragrafo devono rimanere sulla stessa pagina del resto del paragrafo.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Esempi



Mostra come abilitare il controllo vedova/orfano per un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Quando scriviamo il testo che non entra in una pagina, una riga può traboccare nella pagina successiva.
// La singola riga che finisce nella pagina successiva è chiamata "Orphan",
// e la riga precedente dove l'orfano si è interrotto è chiamata "Widow".
// Possiamo correggere orfani e vedove riorganizzando il testo tramite dimensione del carattere, spaziatura o margini di pagina.
// Se desideriamo preservare le dimensioni del nostro documento, possiamo impostare questo flag su "true"
// per spostare le vedove nella stessa pagina del rispettivo orfano.
// Lasciare questo flag su "false" lascerà le coppie vedova/orfano nel testo.
// Ogni paragrafo ha questa impostazione accessibile in Microsoft Word tramite Home -> Paragraph -> Paragraph Settings
// (pulsante nell'angolo in basso a destra della scheda "Paragraph") -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Inserisci del testo che genera un orfano e una vedova.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
