---
title: "Méthode Aspose::Words::DocumentBase::get_PageColor"
linktitle: "get_PageColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBase::get_PageColor. Obtient ou définit la couleur de la page du document. Cette propriété est une version simplifiée de BackgroundShape en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Obtient ou définit la couleur de la page du document. Cette propriété est une version simplifiée de [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Remarques


Cette propriété offre un moyen simple de spécifier une couleur de page unie pour le document. La définir crée et applique une [BackgroundShape](../get_backgroundshape/) appropriée.

Si la couleur de la page n'est pas définie (par ex. il n'y a aucune forme d'arrière-plan dans le document), renvoie **Empty**.

## Exemples



Montre comment définir la couleur d'arrière-plan pour toutes les pages d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## Voir aussi

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
