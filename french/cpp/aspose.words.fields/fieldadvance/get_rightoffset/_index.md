---
title: "Aspose::Words::Fields::FieldAdvance::get_RightOffset méthode"
linktitle: "get_RightOffset"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldAdvance::get_RightOffset méthode. Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé vers la droite en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/fieldadvance/get_rightoffset/
---
## FieldAdvance::get_RightOffset method


Obtient ou définit le nombre de points de déplacement vers la droite du texte qui suit le champ.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_RightOffset()
```


## Exemples



Montre comment insérer un champ ADVANCE et modifier ses propriétés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Ci-dessous deux façons d'utiliser le champ ADVANCE pour ajuster la position du texte qui le suit.
// Les effets d'un champ ADVANCE continuent de s'appliquer jusqu'à la fin du paragraphe,
// ou qu'un autre champ ADVANCE met à jour les valeurs de décalage/coordonnées.
// 1 -  Spécifier un décalage directionnel :
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Déplacer le texte vers une position spécifiée par des coordonnées :
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Voir aussi

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
