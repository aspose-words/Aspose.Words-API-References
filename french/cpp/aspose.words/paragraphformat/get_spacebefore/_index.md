---
title: "Aspose::Words::ParagraphFormat::get_SpaceBefore méthode"
linktitle: "get_SpaceBefore"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_SpaceBefore méthode. Obtient ou définit la quantité d’espacement (en points) avant le paragraphe en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words/paragraphformat/get_spacebefore/
---
## ParagraphFormat::get_SpaceBefore method


Obtient ou définit la quantité d’espacement (en points) avant le paragraphe.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceBefore()
```

## Remarques


N’a aucun effet lorsque [SpaceBeforeAuto](../get_spacebeforeauto/) est **true**.

Les valeurs valides vont de 0 à 1584 inclus.

## Exemples



Montre comment définir l'espacement automatique des paragraphes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Appliquez une grande quantité d'espacement avant et après les paragraphes que ce constructeur créera.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Définissez ces indicateurs sur "true" pour appliquer l'espacement automatique,
// en ignorant effectivement l'espacement dans les propriétés que nous avons définies ci-dessus.
// Les laisser à "false" appliquera notre espacement de paragraphe personnalisé.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Insérez deux paragraphes qui auront un espacement au-dessus et en dessous d'eux et enregistrez le document.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


Montre comment appliquer aucun espacement entre les paragraphes avec le même style.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Appliquez une grande quantité d'espacement avant et après les paragraphes que ce constructeur créera.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Définissez le drapeau "NoSpaceBetweenParagraphsOfSameStyle" sur "vrai" pour appliquer
// aucun espacement entre les paragraphes avec le même style, ce qui regroupera les paragraphes similaires.
// Laissez le drapeau "NoSpaceBetweenParagraphsOfSameStyle" sur "faux"
// pour appliquer uniformément l'espacement à chaque paragraphe.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
