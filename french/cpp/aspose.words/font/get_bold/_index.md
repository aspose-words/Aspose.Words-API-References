---
title: "Méthode Aspose::Words::Font::get_Bold"
linktitle: "get_Bold"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Bold. Vrai si la police est formatée en gras en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


Vrai si la police est formatée en gras.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Exemples



Montre comment insérer du texte formaté en utilisant [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Spécifiez le formatage de la police, puis ajoutez du texte.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
