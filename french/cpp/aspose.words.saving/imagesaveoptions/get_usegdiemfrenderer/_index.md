---
title: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer méthode"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer méthode. Obtient ou définit une valeur déterminant s'il faut utiliser le rendu de métafichier GDI+ ou Aspose.Words lors de l'enregistrement au format EMF en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Obtient ou définit une valeur déterminant s'il faut utiliser le rendu GDI+ ou le rendu de métafichier Aspose.Words lors de l'enregistrement au format EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Remarques


Si réglé sur **true**, le rendu de métafichier GDI+ est utilisé. C.-à-d. le contenu est écrit dans un objet graphique GDI+ et enregistré dans le métafichier.

Si réglé sur **false**, le rendu de métafichier Aspose.Words est utilisé. C.-à-d. le contenu est écrit directement au format métafichier avec Aspose.Words.

N'a d'effet que lors de l'enregistrement au format EMF.

L'enregistrement GDI+ ne fonctionne que sur .NET.

La valeur par défaut est **true**.

## Exemples



Montre comment choisir un rendu lors de la conversion d'un document en .emf.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Lorsque nous enregistrons le document en tant qu'image EMF, nous pouvons transmettre un objet SaveOptions pour sélectionner un rendu pour l'image.
// Si nous définissons le drapeau "UseGdiEmfRenderer" sur "true", Aspose.Words utilisera le rendu GDI+.
// Si nous définissons le drapeau \"UseGdiEmfRenderer\" sur \"false\", Aspose.Words utilisera son propre moteur de rendu de métafichiers.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## Voir aussi

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
