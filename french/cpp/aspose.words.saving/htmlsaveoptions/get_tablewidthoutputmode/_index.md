---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode méthode"
linktitle: "get_TableWidthOutputMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode méthode. Contrôle la façon dont les largeurs des tables, lignes et cellules sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est All en C++."
type: docs
weight: 47000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Contrôle la façon dont les largeurs des tables, lignes et cellules sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Remarques


Dans le format HTML, les éléments de table, de ligne et de cellule (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) peuvent avoir leurs largeurs spécifiées soit en unités relatives (pourcentage) soit en unités absolues. Dans un document Aspose.Words, les tables, lignes et cellules peuvent également avoir leurs largeurs spécifiées en utilisant des unités relatives ou absolues.

Lorsque vous convertissez un document en HTML à l'aide d'Aspose.Words, vous pouvez souhaiter contrôler la façon dont les largeurs des tables, lignes et cellules sont exportées afin d'influencer l'affichage du document résultant dans l'agent visuel (par ex. un navigateur ou un visualiseur).

Utilisez cette propriété comme filtre pour spécifier quelles valeurs de largeur de table sont exportées vers le document de destination. Par exemple, si vous convertissez un document en EPUB et prévoyez de le visualiser sur un appareil de lecture mobile, vous voudrez probablement éviter d'exporter des valeurs de largeur absolues. Pour ce faire, vous devez spécifier le mode de sortie [RelativeOnly](../../htmlelementsizeoutputmode/) ou [None](../../htmlelementsizeoutputmode/) afin que le visualiseur sur l'appareil mobile puisse mettre en page la table pour qu'elle s'adapte au mieux à la largeur de l'écran.

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

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
