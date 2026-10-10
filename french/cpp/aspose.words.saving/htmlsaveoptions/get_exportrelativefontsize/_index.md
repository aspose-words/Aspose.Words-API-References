---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize"
linktitle: "get_ExportRelativeFontSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize. Indique si les tailles de police doivent être émises en unités relatives lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est false en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


Spécifie si les tailles de police doivent être émises en unités relatives lors de l’enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Remarques


Dans de nombreux documents existants (HTML, IDPF EPUB), les tailles de police sont spécifiées en unités relatives. Cela permet aux applications d'ajuster la taille du texte lors de la visualisation ou du traitement des documents. Par exemple, Microsoft Internet Explorer possède le sous‑menu "View->Text Size", Adobe Digital Editions propose deux boutons : Augmenter/Diminuer la taille du texte. Si vous souhaitez que cette fonctionnalité fonctionne, définissez la propriété [ExportRelativeFontSize](./) sur **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

Lorsque cette option est activée, les éléments du document autres que le texte conservent des tailles absolues. De plus, certains attributs liés au texte peuvent être exprimés de manière absolue. En particulier, l'interligne spécifié avec la règle "exactly" peut produire des résultats indésirables lors du redimensionnement du texte. Ainsi, les documents source doivent être correctement conçus et testés lors de l'exportation avec [ExportRelativeFontSize](./) réglé sur **true**.

## Exemples



Montre comment utiliser des tailles de police relatives lors de l'enregistrement au format .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// Lorsque nous enregistrons le document au format HTML, nous pouvons transmettre un objet SaveOptions
// pour déterminer s'il faut utiliser des tailles de police relatives ou absolues.
// Définissez le drapeau "ExportRelativeFontSize" sur "true" pour déclarer les tailles de police
// en utilisant l'unité de mesure "em", qui est un facteur multipliant la taille de police actuelle.
// Définissez le drapeau "ExportRelativeFontSize" sur "false" pour déclarer les tailles de police
// en utilisant l'unité de mesure "pt", qui correspond à la taille absolue de la police en points.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
