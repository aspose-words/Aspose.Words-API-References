---
title: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator méthode"
linktitle: "get_SequenceSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator méthode. Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.fields/fieldtoc/get_sequenceseparator/
---
## FieldToc::get_SequenceSeparator method


Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_SequenceSeparator()
```


## Exemples



Montre comment remplir un champ TOC avec des entrées en utilisant des champs SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
// Chaque entrée contient le paragraphe qui inclut le champ SEQ ainsi que le numéro de page où le champ apparaît.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
// Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique.
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Utilisez la propriété "TableOfFiguresLabel" pour nommer une séquence principale pour la table des matières.
// Maintenant, cette table des matières ne créera des entrées qu'à partir des champs SEQ dont la "SequenceIdentifier" est définie sur "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Nous pouvons nommer une autre séquence de champ SEQ dans la propriété "PrefixedSequenceIdentifier".
// Les champs SEQ de cette séquence préfixe ne créeront pas d'entrées dans la table des matières.
// Chaque entrée de la table des matières créée à partir d'un champ SEQ de séquence principale affichera désormais également le compte qui
// la séquence préfixe est actuellement au niveau du champ SEQ de séquence principale qui a créé l'entrée.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Chaque entrée de la table des matières affichera le compte de la séquence préfixe immédiatement à gauche
// du numéro de page sur lequel apparaît le champ SEQ de séquence principale.
// Nous pouvons spécifier un séparateur personnalisé qui apparaîtra entre ces deux nombres.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Il existe deux façons d'utiliser les champs SEQ pour remplir cette table des matières.
// 1 -  Insertion d'un champ SEQ appartenant à la séquence préfixe de la table des matières :
// Ce champ incrémentera le compte de la séquence SEQ pour "PrefixSequence" de 1.
// Puisque ce champ n'appartient pas à la séquence principale identifiée
// par la propriété "TableOfFiguresLabel" de la table des matières, il n'apparaîtra pas comme une entrée.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Insertion d'un champ SEQ appartenant à la séquence principale de la table des matières :
// Ce champ SEQ créera une entrée dans la table des matières.
// L'entrée de la table des matières contiendra le paragraphe contenant le champ SEQ ainsi que le numéro de la page sur laquelle il apparaît.
// Cette entrée affichera également le compte auquel la séquence préfixe est actuellement à,
// séparé du numéro de page par la valeur de la propriété SeqenceSeparator de la table des matières.
// Le compte "PrefixSequence" est à 1, ce champ SEQ de séquence principale est à la page 2,
// et le séparateur est ">", donc l'entrée affichera "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Insérez une page, avancez la séquence préfixe de 2, puis insérez un champ SEQ pour créer une entrée de table des matières ensuite.
// La séquence préfixe est maintenant à 2, et le champ SEQ de séquence principale est à la page 3,
// ainsi l'entrée de la table des matières affichera "2>3" dans son compteur de pages.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Voir aussi

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
