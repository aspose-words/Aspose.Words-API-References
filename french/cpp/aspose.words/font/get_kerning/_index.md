---
title: "Méthode Aspose::Words::Font::get_Kerning"
linktitle: "get_Kerning"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Kerning. Obtient ou définit la taille de police à laquelle le crénage commence en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Obtient ou définit la taille de police à laquelle le crénage commence.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Exemples



Montre comment spécifier la taille de police à laquelle le crénage commence à prendre effet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Définissez la taille de police du constructeur, ainsi que la taille minimale à laquelle le crénage prendra effet.
// La taille de police descend en dessous du seuil de crénage, donc le segment ci‑dessous n’aura pas de crénage.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Définissez le seuil de crénage afin que la taille de police actuelle du constructeur soit au‑dessus.
// Tout texte que nous ajoutons à partir de ce point aura le crénage appliqué. Les espaces entre les caractères
// seront ajustés, ce qui donne généralement un segment de texte légèrement plus esthétique.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
