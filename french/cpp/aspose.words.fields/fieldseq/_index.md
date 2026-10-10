---
title: "Aspose::Words::Fields::FieldSeq classe"
linktitle: "FieldSeq"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldSeq classe. Implémente le champ SEQ. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 91000
url: /fr/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


Implémente le champ SEQ. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtient ou définit le nom d'un signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Obtient ou définit s'il faut insérer le numéro de séquence suivant pour l'élément spécifié. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Obtient ou définit un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent. |
| [get_ResetNumber](./get_resetnumber/)() | Obtient ou définit un nombre entier auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Obtient ou définit le nom attribué à la série d'éléments qui doivent être numérotés. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

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


Montre comment combiner la table des matières et les champs de séquence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
// Chaque entrée contient le paragraphe qui contient le champ SEQ,
// et le numéro de la page où le champ apparaît.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Configurez ce champ TOC pour qu'il possède une propriété SequenceIdentifier avec la valeur "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Configurez ce champ TOC pour ne récupérer que les champs SEQ qui se trouvent à l'intérieur des limites d'un signet
// nommé "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
// Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique.
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Insérez un champ SEQ dont l'identifiant de séquence correspond à celui du TOC
// propriété TableOfFiguresLabel. Ce champ ne créera pas d'entrée dans le TOC car il se trouve en dehors
// des limites du signet désignées par "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" du TOC et se trouve à l'intérieur des limites du signet.
// Le paragraphe contenant ce champ apparaîtra dans le TOC en tant qu'entrée.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// La séquence de ce champ SEQ ne correspond pas à la propriété "TableOfFiguresLabel" du TOC,
// et se trouve à l'intérieur des limites du signet. Son paragraphe n'apparaîtra pas dans le TOC en tant qu'entrée.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" du TOC et se trouve à l'intérieur des limites du signet.
// Ce champ fait également référence à un autre signet. Le contenu de ce signet apparaîtra dans l'entrée du TOC pour ce champ SEQ.
// Le champ SEQ lui‑même n'affichera pas le contenu de ce signet.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Créez un signet avec un contenu qui apparaîtra dans l'entrée du TOC en raison du champ SEQ ci‑dessus qui le référence.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
