---
title: "Aspose::Words::Fields::FieldNoteRef class"
linktitle: "FieldNoteRef"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldNoteRef class. Implémente le champ NOTEREF. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 72000
url: /fr/cpp/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class


Implémente le champ NOTEREF. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldNoteRef : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtient le nom du signet. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Obtient si l'on doit insérer un hyperlien vers le paragraphe signet. |
| [get_InsertReferenceMark](./get_insertreferencemark/)() | Insère la marque de référence avec le même formatage de caractères que le style Référence de note de bas de page ou Référence de note de fin. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Obtient si l'on doit insérer une position relative du paragraphe signet. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définit le nom du signet. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Définit si l'on doit insérer un hyperlien vers le paragraphe signet. |
| [set_InsertReferenceMark](./set_insertreferencemark/)(bool) | Insère la marque de référence avec le même formatage de caractères que le style Référence de note de bas de page ou Référence de note de fin. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Définit si l'on doit insérer une position relative du paragraphe signet. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

## Exemples



Montre comment référencer des notes de bas de page avec le champ NOTEREF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"CrossReference: ");

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldNoteRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNoteRef, false));
// <--- ne pas mettre à jour le champ
field->set_BookmarkName(u"CrossRefBookmark");
field->set_InsertHyperlink(true);
field->set_InsertReferenceMark(true);
field->set_InsertRelativePosition(false);
builder->Writeln();

builder->StartBookmark(u"CrossRefBookmark");
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Cross referenced footnote.");
builder->EndBookmark(u"CrossRefBookmark");
builder->Writeln();

doc->UpdateFields();

// Ce champ ne fonctionne que dans les anciennes versions de Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Field.NOTEREF.doc");
```

## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
