---
title: "Aspose::Words::Fields::FieldDdeAuto classe"
linktitle: "FieldDdeAuto"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldDdeAuto classe. Implémente le champ DDEAUTO. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class


Implémente le champ DDEAUTO. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDdeAuto : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Obtient si l'objet lié doit être inséré en tant que bitmap. |
| [get_InsertAsHtml](./get_insertashtml/)() | Obtient si l'objet lié doit être inséré en texte au format HTML. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Obtient si l'objet lié doit être inséré en tant qu'image. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Obtient si l'objet lié doit être inséré au format texte enrichi (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Obtient si l'objet lié doit être inséré au format texte uniquement. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Obtient si l'objet lié doit être inséré en texte Unicode. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLinked](./get_islinked/)() | Obtient si la taille du fichier doit être réduite en ne stockant pas les données graphiques avec le document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_ProgId](./get_progid/)() | Obtient le type d'application des informations de lien. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtient le nom et l'emplacement du fichier source. |
| [get_SourceItem](./get_sourceitem/)() | Obtient la partie du fichier source qui est liée. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Définit si l'objet lié doit être inséré en tant que bitmap. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Définit si l'objet lié doit être inséré en texte au format HTML. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Définit si l'objet lié doit être inséré en tant qu'image. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Définit si l'objet lié doit être inséré au format texte enrichi (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | Définit si l'objet lié doit être inséré au format texte uniquement. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Définit si l'objet lié doit être inséré en texte Unicode. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Définit si la taille du fichier doit être réduite en ne stockant pas les données graphiques avec le document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Définit le type d'application des informations de lien. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Définit le nom et l'emplacement du fichier source. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Définit la partie du fichier source qui est liée. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
