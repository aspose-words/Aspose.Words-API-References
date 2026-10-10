---
title: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions costruttore"
linktitle: "OoxmlSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions costruttore. Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel formato Docx in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel formato [Docx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
```


## Esempi



Mostra come impostare una specifica di conformità OOXML a cui aderire per un documento salvato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se configuriamo le opzioni di compatibilità per conformarci a Microsoft Word 2003,
// l'inserimento di un'immagine definirà la sua forma usando VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Lo standard OOXML "ISO/IEC 29500:2008" non supporta forme VML.
// Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
// qualsiasi documento che salviamo passando questo oggetto dovrà seguire tale standard.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Il nostro documento salvato definisce la forma usando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## Vedi anche

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nei formati [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) o [FlatOpc](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Può essere [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) o [FlatOpc](../../../aspose.words/saveformat/). |

## Esempi



Mostra come supportare i caratteri di controllo legacy durante la conversione in .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e poi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "KeepLegacyControlChars" su "true" per preservare
// il carattere legacy "ShortDateTime" durante il salvataggio.
// Imposta la proprietà "KeepLegacyControlChars" su "false" per rimuovere
// il carattere legacy "ShortDateTime" dal documento di output.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
