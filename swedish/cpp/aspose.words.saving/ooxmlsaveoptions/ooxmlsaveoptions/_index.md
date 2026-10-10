---
title: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions konstruktör"
linktitle: "OoxmlSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions konstruktör. Initierar en ny instans av denna klass som kan användas för att spara ett dokument i Docx‑formatet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Docx](../../../aspose.words/saveformat/) formatet.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
```


## Exempel



Visar hur man anger en OOXML-efterlevnadsspecifikation för ett sparat dokument att följa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Om vi konfigurerar kompatibilitetsalternativ för att följa Microsoft Word 2003,
// kommer infogning av en bild att definiera dess form med VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Standarden "ISO/IEC 29500:2008" för OOXML stödjer inte VML-former.
// Om vi sätter egenskapen "Compliance" för SaveOptions-objektet till "OoxmlCompliance.Iso29500_2008_Strict",
// kommer alla dokument vi sparar medan vi passerar detta objekt att behöva följa den standarden.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Vårt sparade dokument definierar formen med DML för att följa standarden "ISO/IEC 29500:2008" för OOXML.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## Se även

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) eller [FlatOpc](../../../aspose.words/saveformat/) formatet.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kan vara [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) eller [FlatOpc](../../../aspose.words/saveformat/). |

## Exempel



Visar hur man stödjer äldre kontrolltecken vid konvertering till .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions‑objekt.
// och sedan skicka den till dokumentets sparningsmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "KeepLegacyControlChars" till "true" för att bevara
// det "ShortDateTime" legacytecknet vid sparande.
// Ställ in egenskapen "KeepLegacyControlChars" till "false" för att ta bort
// det "ShortDateTime" legacytecknet från utdata-dokumentet.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
