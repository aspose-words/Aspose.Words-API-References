---
title: "Metodo Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text"
linktitle: "get_RecognizeUtf8Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text. Quando impostato su true, proverà a rilevare i caratteri UTF8, che saranno preservati durante l'importazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


Quando impostato su **true**, cercherà di rilevare i caratteri UTF8, che saranno preservati durante l'importazione.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Note


Il valore predefinito è **false**.

## Esempi



Mostra come rilevare i caratteri UTF-8 durante il caricamento di un documento RTF.
```cpp
// Crea un oggetto "RtfLoadOptions" per modificare il modo in cui carichiamo un documento RTF.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Imposta la proprietà "RecognizeUtf8Text" su "false" per assumere che il documento utilizzi il set di caratteri ISO 8859-1
// e carica ogni carattere nel documento.
// Imposta la proprietà "RecognizeUtf8Text" su "true" per analizzare eventuali caratteri a lunghezza variabile che possono comparire nel testo.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Vedi anche

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
