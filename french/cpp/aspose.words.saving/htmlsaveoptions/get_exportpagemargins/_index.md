---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins méthode"
linktitle: "get_ExportPageMargins"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins méthode. Spécifie si les marges de page sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est false en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Spécifie si les marges de page sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Exemples



Montre comment afficher les objets hors limites dans les documents HTML de sortie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un constructeur pour insérer une forme sans habillage.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Des valeurs de position négatives de la forme peuvent placer la forme en dehors des limites de la page.
// Si nous exportons cela en HTML, la forme apparaîtra tronquée.
shape->set_Left(-150);

// Lors de l'enregistrement du document au format HTML, nous pouvons passer un objet SaveOptions
// pour décider s'il faut ajuster la page afin d'afficher pleinement les objets hors limites.
// Si nous définissons le drapeau "ExportPageMargins" sur "true", la forme sera entièrement visible dans le HTML de sortie.
// Si nous définissons le drapeau "ExportPageMargins" sur "false",
// notre document affichera la forme tronquée comme nous la verrions dans Microsoft Word.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
