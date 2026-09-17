---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method. Obtient ou définit une valeur booléenne indiquant s'il est permis de remplacer le saut de paragraphe lorsqu'il n'existe pas de paragraphe frère suivant. La valeur par défaut est false en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Obtient ou définit une valeur booléenne indiquant s'il est autorisé de remplacer le saut de paragraphe lorsqu'il n'existe pas de paragraphe frère suivant. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Exemples



Montre comment supprimer un paragraphe d'une cellule de tableau contenant un tableau imbriqué.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créer un tableau avec un paragraphe et un tableau interne dans la première cellule.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// Lorsque l'option suivante est définie sur 'true', Aspose.Words supprimera le texte du paragraphe
// complètement avec sa marque de paragraphe. Sinon, Aspose.Words imitera Word et supprimera
// seulement le texte du paragraphe et laissera la marque de paragraphe intacte (lorsqu'un tableau suit le texte).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
