---
title: "Aspose::Words::Border::get_Color méthode"
linktitle: "get_Color"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border::get_Color méthode. Obtient ou définit la couleur de la bordure en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/border/get_color/
---
## Border::get_Color method


Obtient ou définit la couleur de la bordure.

```cpp
System::Drawing::Color Aspose::Words::Border::get_Color()
```


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
