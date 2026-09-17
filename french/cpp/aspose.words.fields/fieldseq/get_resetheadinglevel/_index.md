---
title: "Méthode Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel"
linktitle: "get_ResetHeadingLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel. Obtient ou définit un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldseq/get_resetheadinglevel/
---
## FieldSeq::get_ResetHeadingLevel method


Obtient ou définit un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel()
```


## Exemples



Affiche la création de numérotation à l'aide des champs SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
// Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique.
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Insérez un champ SEQ qui affichera la valeur actuelle du compteur de "MySequence",
// après avoir utilisé la propriété "ResetNumber" pour le définir à 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Affichez le numéro suivant de cette séquence avec un autre champ SEQ.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Insérez un titre de niveau 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Insérez un autre champ SEQ de la même séquence et configurez-le pour réinitialiser le compteur à chaque titre avec 1.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Le titre ci‑dessus est un titre de niveau 1, donc le compteur de cette séquence est réinitialisé à 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Passez au numéro suivant de cette séquence.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```

## Voir aussi

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
