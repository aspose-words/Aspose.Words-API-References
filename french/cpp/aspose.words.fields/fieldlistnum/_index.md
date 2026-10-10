---
title: "Aspose::Words::Fields::FieldListNum class"
linktitle: "FieldListNum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldListNum class. Implémente le champ LISTNUM. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 64000
url: /fr/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


Implémente le champ LISTNUM. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
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
| [get_HasListName](./get_haslistname/)() | Renvoie une valeur indiquant si le nom d'une définition de numérotation abstraite est fourni par le code du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_ListLevel](./get_listlevel/)() | Obtient ou définit le niveau dans la liste, en remplaçant le comportement par défaut du champ. |
| [get_ListName](./get_listname/)() | Obtient ou définit le nom de la définition de numérotation abstraite utilisée pour la numérotation. |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_StartingNumber](./get_startingnumber/)() | Obtient ou définit la valeur de départ pour ce champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

## Exemples



Montre comment numéroter les paragraphes avec les champs LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les champs LISTNUM affichent un nombre qui s’incrémente à chaque champ LISTNUM.
// Ces champs offrent également une variété d’options qui nous permettent de les utiliser pour émuler des listes numérotées.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Les listes commencent à compter à 1 par défaut, mais nous pouvons définir ce nombre à une valeur différente, comme 0.
// Ce champ affichera "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// Les champs LISTNUM maintiennent des comptes séparés pour chaque niveau de liste.
// Insérer un champ LISTNUM dans le même paragraphe qu’un autre champ LISTNUM
// augmente le niveau de liste au lieu du compte.
// Le champ suivant continuera le compte que nous avons commencé ci‑dessus et affichera la valeur "1" au niveau de liste 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Ce champ démarrera un compte au niveau de liste 2. Il affichera la valeur "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Ce champ démarrera un compte au niveau de liste 3. Il affichera la valeur "1".
// Les différents niveaux de liste ont un formatage différent,
// ainsi ces champs combinés afficheront la valeur "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Le prochain champ LISTNUM que nous insérons continuera le compte au niveau de liste
// sur lequel le champ LISTNUM précédent était.
// Nous pouvons utiliser la propriété "ListLevel" pour passer à un niveau de liste différent.
// Si ce champ LISTNUM restait au niveau de liste 3, il afficherait "ii)",
// mais, comme nous l’avons déplacé au niveau de liste 2, il poursuit le compte à ce niveau et affiche "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Nous pouvons définir la propriété ListName pour que le champ émule un type de champ AUTONUM différent.
// "NumberDefault" émule AUTONUM, "OutlineDefault" émule AUTONUMOUT,
// et "LegalDefault" émule les champs AUTONUMLGL.
// Le nom de liste \"OutlineDefault\" avec 1 comme numéro de départ affichera \"I.\".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// Le ListName ne se transmet pas depuis le champ précédent, nous devrons donc le définir pour chaque nouveau champ.
// Ce champ continue le comptage avec un nom de liste différent et affiche \"II.\".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
