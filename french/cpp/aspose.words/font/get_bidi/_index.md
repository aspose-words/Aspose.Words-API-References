---
title: "Méthode Aspose::Words::Font::get_Bidi"
linktitle: "get_Bidi"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Bidi. Spécifie si le contenu de cette séquence doit avoir des caractéristiques de droite à gauche en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


Spécifie si le contenu de cet enchaînement doit avoir des caractéristiques de droite à gauche.

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## Remarques


Cette propriété, lorsqu'elle est activée, ne doit pas être utilisée avec du texte fortement de gauche à droite. Tout comportement dans cette condition est non spécifié. Cette propriété, lorsqu'elle est désactivée, ne doit pas être utilisée avec du texte fortement de droite à gauche. Tout comportement dans cette condition est non spécifié.

Lorsque le contenu de cette séquence est affiché, tous les caractères doivent être traités comme des caractères d'écriture complexe à des fins de mise en forme. Cela signifie que [BoldBi](../get_boldbi/), [ItalicBi](../get_italicbi/), [SizeBi](../get_sizebi/) et un nom de police correspondant seront utilisés lors du rendu de cette séquence.

De plus, lorsque le contenu de cette séquence est affiché, cette propriété agit comme un remplacement de droite à gauche pour les caractères classés comme « types faibles » et « types neutres ».

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
