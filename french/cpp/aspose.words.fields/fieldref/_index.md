---
title: "Aspose::Words::Fields::FieldRef classe"
linktitle: "FieldRef"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldRef classe. Implémente le champ REF. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 85000
url: /fr/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Implémente le champ REF. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtient ou définit le nom du signet référencé. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](./get_end/)() override | Obtient le nœud qui représente la fin du champ. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Obtient si l'on doit incrémenter les numéros de note de bas de page, de note de fin et d'annotation marqués par le signet, et insérer le texte de note de bas de page, de note de fin et de commentaire correspondant. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Obtient si l'on doit créer un hyperlien vers le paragraphe signeté. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Obtient si l'on doit insérer le numéro du paragraphe référencé exactement tel qu'il apparaît dans le document. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Obtient si l'on doit insérer le numéro du paragraphe référencé dans son contexte complet. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Obtient si l'on doit insérer le numéro du paragraphe référencé dans un contexte relatif. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Obtient si l'on doit insérer la position relative du paragraphe référencé. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_NumberSeparator](./get_numberseparator/)() | Obtient la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](./get_separator/)() override | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](./get_start/)() override | Obtient le nœud qui représente le début du champ. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Obtient si l'on doit supprimer les caractères non délimiteurs. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Définit si l'on doit incrémenter les numéros de note de bas de page, de note de fin et d'annotation marqués par le signet, et insérer le texte de note de bas de page, de note de fin et de commentaire correspondant. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Définit si l'on doit créer un hyperlien vers le paragraphe signeté. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Définit si l'on doit insérer le numéro du paragraphe référencé exactement tel qu'il apparaît dans le document. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Définit si l'on doit insérer le numéro du paragraphe référencé dans son contexte complet. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Définit s'il faut insérer le numéro du paragraphe référencé dans le contexte relatif. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Définit s'il faut insérer la position relative du paragraphe référencé. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Définit s'il faut supprimer les caractères non délimiteurs. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

## Exemples



Montre comment créer du texte signet avec un champ SET, puis l'afficher dans le document à l'aide d'un champ REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nommez le texte signet avec un champ SET.
// Ce champ fait référence au "bookmark" pas à une structure de signet qui apparaît dans le texte, mais à une variable nommée.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Faites référence au signet par son nom dans un champ REF et affichez son contenu.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
