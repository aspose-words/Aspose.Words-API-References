---
title: "Aspose::Words::Font::get_Border méthode"
linktitle: "get_Border"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Border méthode. Retourne un objet Border qui spécifie la bordure pour la Font en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Retourne un objet [Border](../../border/) qui spécifie la bordure pour la Font.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
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

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
