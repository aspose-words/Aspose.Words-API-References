---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation méthode"
linktitle: "get_ExportRoundtripInformation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation méthode. Spécifie s'il faut écrire les informations de cycle lors de l'enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est true pour HTML et false pour MHTML et EPUB en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportroundtripinformation/
---
## HtmlSaveOptions::get_ExportRoundtripInformation method


Spécifie s’il faut écrire les informations de round‑trip lors de l’enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **true** pour HTML et **false** pour MHTML et EPUB.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation() const
```

## Remarques


[Saving](../../) of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

Lorsque **true**, les informations de cycle sont exportées comme propriétés CSS -aw-* des éléments HTML correspondants.

Lorsque **false**, aucune information de cycle n'est générée dans les fichiers produits.

## Exemples



Montre comment préserver les éléments masqués lors de la conversion en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Lors de la conversion d'un document en .html, certains éléments tels que les signets masqués, les positions originales des formes,
// ou les notes de bas de page seront soit supprimés soit convertis en texte brut et seront effectivement perdus.
// En enregistrant avec un objet HtmlSaveOptions dont ExportRoundtripInformation est réglé sur true, ces éléments seront préservés.

// Lorsque nous enregistrons le document en HTML, nous pouvons passer un objet SaveOptions pour déterminer
// comment l'opération d'enregistrement exportera les éléments du document que HTML ne prend pas en charge ou n'utilise pas,
// comme les signets cachés et les positions originales des formes.
// Si nous définissons le drapeau "ExportRoundtripInformation" sur "true", l'opération d'enregistrement préservera ces éléments.
// Si nous définissons le drapeau "ExportRoundTripInformation" sur "false", l'opération d'enregistrement rejettera ces éléments.
// Nous voudrons préserver ces éléments si nous prévoyons de charger le HTML enregistré en utilisant Aspose.Words,
// car ils pourraient être utiles à nouveau.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRoundtripInformation(exportRoundtripInformation);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") + u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; -aw-border-bottom:0.5pt single #000000; " + u"-aw-border-left:0.5pt single #000000; -aw-border-right:6pt single #000000; -aw-border-top:0.5pt single #000000\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" ") + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Page number </span>") + u"<span style=\"-aw-field-start:true\"></span>" + u"<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" + u"<span style=\"-aw-field-separator:true\"></span>" + u"<span>1</span>" + u"<span style=\"-aw-field-end:true\"></span>"));

    ASSERT_EQ(1, doc->get_Range()->get_Fields()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
    {
        return f->get_Type() == Aspose::Words::Fields::FieldType::FieldPage;
    }))));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") + u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    ASSERT_TRUE(outDocContents.Contains(u"<span>Page number 1</span>"));

    ASSERT_EQ(0, doc->get_Range()->get_Fields()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
    {
        return f->get_Type() == Aspose::Words::Fields::FieldType::FieldPage;
    }))));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
