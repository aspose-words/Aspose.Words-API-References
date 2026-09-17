---
title: "Méthode Aspose::Words::ParagraphFormat::get_SpaceAfterAuto"
linktitle: "get_SpaceAfterAuto"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_SpaceAfterAuto. Vrai si la quantité d'espacement après le paragraphe est définie automatiquement en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words/paragraphformat/get_spaceafterauto/
---
## ParagraphFormat::get_SpaceAfterAuto method


Vrai si la quantité d’espacement après le paragraphe est définie automatiquement.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceAfterAuto()
```

## Remarques


Lorsqu'il est défini sur **true**, remplace l'effet de [SpaceAfter](../get_spaceafter/).

Lorsque vous définissez l'Espace avant et l'Espace après du paragraphe sur Auto, **Microsoft** Word ajoute automatiquement un espacement de 14 points entre les paragraphes selon les règles suivantes :

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



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

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
