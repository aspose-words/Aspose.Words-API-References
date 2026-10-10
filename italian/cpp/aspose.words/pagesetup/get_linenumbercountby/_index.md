---
title: "Aspose::Words::PageSetup::get_LineNumberCountBy metodo"
linktitle: "get_LineNumberCountBy"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_LineNumberCountBy metodo. Restituisce o imposta l'incremento numerico per i numeri di riga in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words/pagesetup/get_linenumbercountby/
---
## PageSetup::get_LineNumberCountBy method


Restituisce o imposta l'incremento numerico per i numeri di riga.

```cpp
int32_t Aspose::Words::PageSetup::get_LineNumberCountBy()
```


## Esempi



Mostra come abilitare la numerazione delle righe per una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Possiamo usare l'oggetto PageSetup della sezione per visualizzare i numeri a sinistra delle righe di testo della sezione.
// Questo è lo stesso comportamento di un oggetto List,
// ma copre l'intera sezione e non modifica il testo in alcun modo.
// La nostra sezione riprenderà la numerazione su ogni nuova pagina a partire da 1 e visualizzerà il numero,
// se è un multiplo di 3, a 50pt a sinistra della riga.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// Il contatore delle righe salterà qualsiasi paragrafo con il flag "SuppressLineNumbers" impostato su "true".
// Questo paragrafo è alla 15ª riga, che è un multiplo di 3, e quindi normalmente visualizzerebbe un numero di riga.
// Il contatore delle righe della sezione ignorerà anche questa riga, considererà la riga successiva come la 15ª,
// e continuerà il conteggio da quel punto in poi.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
