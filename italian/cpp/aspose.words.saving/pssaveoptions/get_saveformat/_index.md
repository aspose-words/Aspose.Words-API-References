---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat metodo"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat metodo. Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio viene utilizzato. Può essere solo Ps in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio viene utilizzato. Può essere solo [Ps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


## Esempi



Mostra come salvare un documento nel formato Postscript sotto forma di piegatura a libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Crea un oggetto "PsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in PostScript.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare i contenuti
// nel documento Postscript di output in modo da poter creare un libretto.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "false" per salvare il documento normalmente.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Se stiamo rendendo il documento come libretto, dobbiamo impostare "MultiplePages"
// proprietà degli oggetti di configurazione pagina di tutte le sezioni a "MultiplePagesType.BookFoldPrinting".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Una volta stampato questo documento su entrambi i lati delle pagine, possiamo piegare tutte le pagine a metà contemporaneamente,
// e il contenuto si allineerà in modo da creare un libretto.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
