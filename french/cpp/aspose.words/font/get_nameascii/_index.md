---
title: "Méthode Aspose::Words::Font::get_NameAscii"
linktitle: "get_NameAscii"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_NameAscii. Retourne ou définit la police utilisée pour le texte latin (caractères avec des codes de caractères de 0 (zéro) à 127) en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words/font/get_nameascii/
---
## Font::get_NameAscii method


Renvoie ou définit la police utilisée pour le texte latin (caractères avec des codes de caractères de 0 (zéro) à 127).

```cpp
System::String Aspose::Words::Font::get_NameAscii()
```


## Exemples



Montre comment Microsoft Word peut combiner deux polices différentes dans un même segment.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Supposons un segment que nous utilisons le constructeur pour insérer en utilisant cette configuration de police
// contient des caractères dans la plage des caractères ASCII. Dans ce cas,
// il affichera ces caractères en utilisant cette police.
builder->get_Font()->set_NameAscii(u"Calibri");

// Sans autre police spécifiée, le constructeur appliquera également cette police à tous les caractères qu'il insère.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Spécifiez une police à utiliser pour tous les caractères en dehors de la plage ASCII.
// Idéalement, cette police devrait posséder un glyphe pour chaque code de caractère non-ASCII requis.
builder->get_Font()->set_NameOther(u"Courier New");

// Insérez un segment avec un mot composé de caractères ASCII, et un mot avec tous les caractères en dehors de cette plage.
// Chaque caractère sera affiché en utilisant l'une ou l'autre des polices, selon.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
