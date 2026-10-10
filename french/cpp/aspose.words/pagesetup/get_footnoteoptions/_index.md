---
title: "Aspose::Words::PageSetup::get_FootnoteOptions méthode"
linktitle: "get_FootnoteOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_FootnoteOptions méthode. Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans cette section en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words/pagesetup/get_footnoteoptions/
---
## PageSetup::get_FootnoteOptions method


Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans cette section.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> Aspose::Words::PageSetup::get_FootnoteOptions()
```


## Exemples



Montre comment configurer les options affectant les notes de bas de page/notes de fin dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Configurez toutes les notes de bas de page dans la première section pour recommencer la numérotation à partir de 1
// à chaque nouvelle page et les afficher directement sous le texte sur chaque page.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Configurez toutes les notes de fin dans la première section pour maintenir un compte continu tout au long de la section,
// à partir de 1. De plus, définissez-les tous pour qu’ils apparaissent regroupés à la fin du document.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## Voir aussi

* Class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
