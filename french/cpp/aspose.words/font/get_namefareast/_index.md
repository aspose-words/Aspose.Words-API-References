---
title: "Méthode Aspose::Words::Font::get_NameFarEast"
linktitle: "get_NameFarEast"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_NameFarEast. Retourne ou définit un nom de police d'Asie de l'Est en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


Renvoie ou définit un nom de police d'Asie de l'Est.

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## Exemples



Montre comment insérer et formater du texte dans une langue d'Extrême-Orient.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Spécifiez les paramètres de police que le constructeur de documents appliquera à tout texte qu'il insère.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Nommez les équivalents "FarEast" pour notre police et notre paramètre régional.
// Si le constructeur insère des caractères asiatiques avec cette configuration de police, alors chaque segment qui contient
// ces caractères les affichera en utilisant la police/paramètre régional "FarEast" au lieu de la valeur par défaut.
// Cela peut être utile lorsqu'une police occidentale ne possède pas de représentations idéales pour les caractères asiatiques.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Ce texte sera affiché avec la police/paramètre régional par défaut.
builder->Writeln(u"Hello world!");

// Étant donné qu'il s'agit de caractères asiatiques, ce segment appliquera nos équivalents de police/paramètre régional "FarEast".
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
