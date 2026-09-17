---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers"
linktitle: "get_ExportTocPageNumbers"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers. Spécifie s'il faut écrire les numéros de page dans la table des matières lors de l'enregistrement en HTML, MHTML et EPUB. La valeur par défaut est false en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Spécifie s’il faut écrire les numéros de page dans la table des matières lors de l’enregistrement en HTML, MHTML et EPUB. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Exemples



Montre comment afficher les numéros de page lors de l'enregistrement d'un document avec une table des matières au format .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une table des matières, puis remplissez le document avec des paragraphes formatés à l'aide d'un "Heading"
// style que la table des matières reconnaîtra comme entrées. Chaque entrée affichera le paragraphe de titre à gauche,
// et le numéro de page contenant le titre à droite.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// Les documents HTML n'ont pas de pages. Si nous enregistrons ce document en HTML,
// les numéros de page affichés par notre table des matières n'auront aucun sens.
// Lorsque nous enregistrons le document en HTML, nous pouvons passer un objet SaveOptions pour omettre ces numéros de page de la table des matières.
// Si nous définissons le drapeau "ExportTocPageNumbers" sur "true",
// chaque entrée de la table des matières affichera le titre, le séparateur et le numéro de page, préservant ainsi son apparence dans Microsoft Word.
// Si nous définissons le drapeau "ExportTocPageNumbers" sur "false",
// l'opération d'enregistrement omettra à la fois le séparateur et le numéro de page et laissera le titre de chaque entrée intact.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
