---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments vers HTML, MHTML et EPUB en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments vers HTML, MHTML et EPUB.

```cpp
enum class HtmlElementSizeOutputMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Tous | 0 | Toutes les tailles d'éléments, à la fois en unités absolues et relatives, spécifiées dans le document sont exportées. |
| RelativeOnly | 1 | Les tailles d'éléments sont exportées uniquement si elles sont spécifiées en unités relatives dans le document. Les tailles fixes ne sont pas exportées dans ce mode. Les agents visuels calculeront les tailles manquantes pour rendre la mise en page du document plus naturelle. |
| None | 2 | Les tailles d'éléments ne sont pas exportées. Les agents visuels construiront la mise en page automatiquement en fonction de la relation entre les éléments. |


## Exemples



Montre comment préserver les retraits négatifs dans le .html de sortie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un tableau avec un retrait négatif, ce qui le poussera vers la gauche au-delà de la marge gauche de la page.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Insérez un tableau avec un retrait positif, ce qui poussera le tableau vers la droite.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// Lorsque nous enregistrons un document au format HTML, Aspose.Words ne préservera que les retraits négatifs
// comme celui que nous avons appliqué au premier tableau si nous définissons le drapeau "AllowNegativeIndent"
// dans un objet SaveOptions que nous passerons à "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
