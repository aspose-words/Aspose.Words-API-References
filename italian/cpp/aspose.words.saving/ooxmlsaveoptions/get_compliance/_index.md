---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance metodo"
linktitle: "get_Compliance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance metodo. Specifica la versione OOXML per il documento di output. Il valore predefinito è Ecma376_2006 in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/get_compliance/
---
## OoxmlSaveOptions::get_Compliance method


Specifica la versione OOXML per il documento di output. Il valore predefinito è [Ecma376_2006](../../ooxmlcompliance/).

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance()
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


Mostra come configurare un elenco per riavviare la numerazione in ogni sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// La proprietà "IsRestartAtEachSection" sarà applicabile solo quando
// il livello di conformità OOXML del documento è impostato su uno standard più recente di "OoxmlComplianceCore.Ecma376".
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```


Mostra come inserire forme DML in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 -  Fluttuante:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  In linea:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Se è necessario creare forme "non-primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// quindi salva il documento con conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Vedi anche

* Enum [OoxmlCompliance](../../ooxmlcompliance/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
