---
title: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle méthode"
linktitle: "get_NoSpaceBetweenParagraphsOfSameStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle méthode. Lorsque **vrai**, SpaceBefore et SpaceAfter seront ignorés entre les paragraphes du même style en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words/paragraphformat/get_nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method


Lorsque **vrai**, [SpaceBefore](../get_spacebefore/) et [SpaceAfter](../get_spaceafter/) seront ignorés entre les paragraphes du même style.

```cpp
bool Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle()
```

## Remarques


Ce paramètre ne prend effet que lorsqu'il est appliqué à un style de paragraphe. S'il est appliqué directement à un paragraphe, il n'a aucun effet.

## Exemples



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
