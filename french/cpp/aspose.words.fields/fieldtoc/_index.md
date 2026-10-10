---
title: "Aspose::Words::Fields::FieldToc classe"
linktitle: "FieldToc"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldToc classe. Implémente le champ TOC. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 105000
url: /fr/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Implémente le champ TOC. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Obtient le nom du signet qui marque la partie du document utilisée pour construire le tableau. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'une table des figures qui n'inclut pas l'étiquette et le numéro de la légende. |
| [get_CustomStyles](./get_customstyles/)() | Obtient une liste de styles autres que les styles de titres intégrés à inclure dans la table des matières. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Obtient une chaîne qui doit correspondre aux identifiants de type des champs TC inclus. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Obtient une plage de niveaux des entrées de la table des matières à inclure. |
| [get_EntrySeparator](./get_entryseparator/)() | Obtient une séquence de caractères qui sépare une entrée de son numéro de page. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Obtient une plage de niveaux de titres à inclure. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Obtient si l'on doit masquer le leader de tabulation et les numéros de page dans la vue mise en page Web. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Obtient si les entrées de la table des matières doivent être des hyperliens. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Obtient une plage de niveaux des entrées de la table des matières à partir desquels les numéros de page sont omis. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Obtient ou définit l'identifiant d'une séquence pour laquelle un préfixe doit être ajouté au numéro de page de l'entrée. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Obtient si les caractères de saut de ligne doivent être conservés dans les entrées de la table. |
| [get_PreserveTabs](./get_preservetabs/)() | Obtient si les entrées de tabulation doivent être conservées dans les entrées de la table. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'une table des figures. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Obtient si le niveau de plan de paragraphe appliqué doit être utilisé. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définit le nom du signet qui marque la partie du document utilisée pour construire le tableau. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Définit une liste de styles autres que les styles de titres intégrés à inclure dans la table des matières. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Définit une chaîne qui doit correspondre aux identifiants de type des champs TC inclus. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Définit une plage de niveaux des entrées de la table des matières à inclure. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Définit une séquence de caractères qui sépare une entrée de son numéro de page. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Définit une plage de niveaux de titres à inclure. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Définit si le leader de tabulation et les numéros de page doivent être masqués dans la vue mise en page Web. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Définit si les entrées de la table des matières doivent être des hyperliens. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Définit une plage de niveaux des entrées de la table des matières à partir desquels les numéros de page sont omis. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Définit s'il faut conserver les caractères de saut de ligne dans les entrées de la table. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Définit s'il faut conserver les tabulations dans les entrées de la table. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Définit s'il faut utiliser le niveau de plan de paragraphe appliqué. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Met à jour les numéros de page des éléments de cette table des matières. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
