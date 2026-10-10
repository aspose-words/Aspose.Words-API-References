---
title: "Metodo Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo Xps in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/xpssaveoptions/get_saveformat/
---
## XpsSaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat() override
```


## Esempi



Mostra come limitare il livello dei titoli che appariranno nella struttura di un documento XPS salvato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci titoli che possono servire come voci di indice a livelli 1, 2 e poi 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Crea un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare come quel metodo converte il documento in .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Il documento XPS di output conterrà una struttura, un indice che elenca i titoli nel corpo del documento.
// Facendo clic su una voce di questa struttura si verrà portati alla posizione del relativo titolo.
// Imposta la proprietà "HeadingsOutlineLevels" a "2" per escludere tutti i titoli il cui livello è superiore a 2 dalla struttura.
// Gli ultimi due titoli inseriti sopra non appariranno.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
