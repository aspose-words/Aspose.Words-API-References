---
title: "Méthode Aspose::Words::Font::get_BoldBi"
linktitle: "get_BoldBi"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_BoldBi. Vrai si le texte de droite à gauche est formaté en gras dans C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/font/get_boldbi/
---
## Font::get_BoldBi method


Vrai si le texte de droite à gauche est formaté en gras.

```cpp
bool Aspose::Words::Font::get_BoldBi()
```


## Exemples



Montre comment définir des ensembles séparés de paramètres de police pour le texte de droite à gauche, et le texte de droite à gauche.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez un ensemble de paramètres de police pour le texte de gauche à droite.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Définissez un autre ensemble de paramètres de police pour le texte de droite à gauche.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// Nous pouvons également utiliser le drapeau Bidi pour indiquer si le texte que nous allons ajouter
// avec le constructeur de document est de droite à gauche. Lorsque nous ajoutons du texte avec ce drapeau réglé sur vrai,
// il sera formaté en utilisant l'ensemble de paramètres de police de droite à gauche.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Réglez le drapeau sur faux, puis ajoutez du texte de gauche à droite.
// Le constructeur de document les formattera en utilisant l'ensemble de paramètres de police de gauche à droite.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
