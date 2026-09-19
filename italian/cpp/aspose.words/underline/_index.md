---
title: "Aspose::Words::Underline enum"
linktitle: "Sottolineatura"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Underline enum. Indica il tipo di sottolineatura applicata a un carattere in C++."
type: docs
weight: 126000
url: /it/cpp/aspose.words/underline/
---
## Underline enum


Indica il tipo di sottolineatura applicata a un carattere.

```cpp
enum class Underline
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 |  |
| Singola | 1 |  |
| Parole | 2 |  |
| Doppia | 3 |  |
| Punteggiata | 4 |  |
| Spessa | 6 |  |
| Trattino | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


## Esempi



Mostra come inserire un campo collegamento ipertestuale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserisci un collegamento ipertestuale e enfatizzalo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic sinistro sul collegamento nel testo in Microsoft Word ci porterà all'URL tramite una nuova finestra del browser web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
