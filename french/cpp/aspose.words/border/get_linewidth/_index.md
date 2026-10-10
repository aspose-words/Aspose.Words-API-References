---
title: "Aspose::Words::Border::get_LineWidth méthode"
linktitle: "get_LineWidth"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border::get_LineWidth méthode. Obtient ou définit la largeur de la bordure en points en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Obtient ou définit la largeur de la bordure en points.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Remarques


Si vous définissez une largeur de ligne supérieure à zéro lorsque le style de ligne est aucun, le style de ligne est automatiquement changé en ligne simple.

## Exemples



Montre comment insérer une chaîne entourée d'une bordure dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Voir aussi

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
