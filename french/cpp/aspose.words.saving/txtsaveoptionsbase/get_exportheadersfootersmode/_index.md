---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode méthode"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode méthode. Spécifie la façon dont les en-têtes et pieds de page sont exportés vers les formats texte. La valeur par défaut est PrimaryOnly en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/txtsaveoptionsbase/get_exportheadersfootersmode/
---
## TxtSaveOptionsBase::get_ExportHeadersFootersMode method


Spécifie la façon dont les en-têtes et pieds de page sont exportés vers les formats texte. La valeur par défaut est [PrimaryOnly](../../txtexportheadersfootersmode/).

```cpp
Aspose::Words::Saving::TxtExportHeadersFootersMode Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode() const
```


## Exemples



Montre comment spécifier la façon d'exporter les en-têtes et pieds de page au format texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez les en-têtes/pieds de page pairs et principaux dans le document.
// Les en-têtes/pieds de page principaux remplaceront les en-têtes/pieds de page pairs.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Insérez des pages pour afficher ces en-têtes et pieds de page.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Définissez la propriété "ExportHeadersFootersMode" sur "TxtExportHeadersFootersMode.None"
// pour ne pas exporter d'en-têtes/pieds de page.
// Définissez la propriété "ExportHeadersFootersMode" sur "TxtExportHeadersFootersMode.PrimaryOnly"
// pour n'exporter que les en-têtes/pieds de page principaux.
// Définissez la propriété "ExportHeadersFootersMode" sur "TxtExportHeadersFootersMode.AllAtEnd"
// pour placer tous les en-têtes et pieds de page de tous les corps de section à la fin du document.
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt");

System::String newLine = System::Environment::get_NewLine();
switch (txtExportHeadersFootersMode)
{
    case Aspose::Words::Saving::TxtExportHeadersFootersMode::AllAtEnd:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Even header{0}{1}", newLine, newLine) + System::String::Format(u"Primary header{0}{1}", newLine, newLine) + System::String::Format(u"Even footer{0}{1}", newLine, newLine) + System::String::Format(u"Primary footer{0}{1}", newLine, newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::PrimaryOnly:
        ASSERT_EQ(System::String::Format(u"Primary header{0}", newLine) + System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Primary footer{0}", newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::None:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine), docText);
        break;

}
```

## Voir aussi

* Enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
