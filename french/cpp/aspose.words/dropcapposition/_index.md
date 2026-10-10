---
title: "Aspose::Words::DropCapPosition énum"
linktitle: "DropCapPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DropCapPosition énum. Spécifie la position du texte en lettrine en C++."
type: docs
weight: 87000
url: /fr/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Spécifie la position du texte en lettrine.

```cpp
enum class DropCapPosition
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Le paragraphe n'a pas de lettrine. |
| Normal | 1 | La lettrine est positionnée à l'intérieur de la marge du texte sur le paragraphe d'ancrage. |
| Marge | 2 | La lettrine est positionnée à l'extérieur de la marge du texte sur le paragraphe d'ancrage. |


## Exemples



Montre comment créer une lettrine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un paragraphe avec une grande lettre avec laquelle le texte des deuxième et troisième paragraphes commence.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actuellement, les deuxième et troisième paragraphes apparaissent sous le premier.
// Nous pouvons convertir le premier paragraphe en lettrine pour les autres paragraphes via son objet "ParagraphFormat".
// Définissez la propriété "DropCapPosition" sur "DropCapPosition.Margin" pour placer la lettrine
// à l'extérieur de la marge de page du côté gauche si notre texte est de gauche à droite.
// Définissez la propriété "DropCapPosition" sur "DropCapPosition.Normal" pour placer la lettrine à l'intérieur des marges de la page
// et pour envelopper le reste du texte autour de celle-ci.
// "DropCapPosition.None" est l'état par défaut pour tous les paragraphes.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
