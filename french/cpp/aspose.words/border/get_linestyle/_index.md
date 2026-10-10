---
title: "Aspose::Words::Border::get_LineStyle méthode"
linktitle: "get_LineStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border::get_LineStyle méthode. Obtient ou définit le style de la bordure en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Obtient ou définit le style de la bordure.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Remarques


Si vous définissez le style de ligne sur aucun, alors la largeur de ligne est automatiquement réglée à zéro.

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
