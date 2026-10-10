---
title: "metodo Aspose::Words::Saving::OoxmlSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_SaveFormat method. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere Docx, Docm, Dotx, Dotm o FlatOpc in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/get_saveformat/
---
## OoxmlSaveOptions::get_SaveFormat method


Specifică il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) o [FlatOpc](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::OoxmlSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
