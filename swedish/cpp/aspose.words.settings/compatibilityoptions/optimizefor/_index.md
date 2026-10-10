---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor metod"
linktitle: "OptimizeFor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor metod. Tillåter att optimera dokumentinnehållet samt standardbeteendet för Aspose.Words till en specifik version av MS Word. Använd denna metod för att förhindra att MS Word visar \"Compatibility mode\"-fliken vid dokumentladdning. (Observera att du också kan behöva sätta egenskapen Compliance till Iso29500_2008_Transitional eller högre.) i C++."
type: docs
weight: 75000
url: /sv/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


Tillåter att optimera dokumentinnehållet samt standardbeteendet för Aspose.Words till en specifik version av MS Word. Använd denna metod för att förhindra att MS Word visar "Compatibility mode"-fliken vid dokumentladdning. (Observera att du även kan behöva sätta [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/)‑egenskapen till [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) eller högre.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
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


Visar hur man vertikalt justerar textinnehållet i en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" för att
// justera texten i den här textrutan med den övre sidan av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" för att
// justera texten i den här textrutan till mitten av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" för att
// justera texten i den här textrutan till botten av formen.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Den vertikala justeringen av text i textrutor är tillgänglig från Microsoft Word 2007 och framåt.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Se även

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
