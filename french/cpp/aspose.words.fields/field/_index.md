---
title: "Aspose::Words::Fields::Field classe"
linktitle: "Champ"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field classe. Représente un champ de document Microsoft Word. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/field/
---
## Field class


Représente un champ de document Microsoft Word. Pour en savoir plus, consultez l'article de documentation.

```cpp
class Field : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](./get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](./get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](./get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](./get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](./get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](./get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](./get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](./get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](./get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](./get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](./get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](./getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](./getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | Mutateur pour [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Mutateur pour [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Mutateur pour [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Effectue le détachement du champ. |
| [Update](./update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](./update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Remarques


Un champ dans un document Word est une structure complexe composée de plusieurs nœuds incluant le début du champ, le code du champ, le séparateur du champ, le résultat du champ et la fin du champ. Les [Fields](../) peuvent être imbriqués, contenir du contenu riche et s'étendre sur plusieurs paragraphes ou sections d'un document. La classe [Field](./) est un objet « façade » qui fournit des propriétés et des méthodes permettant de travailler avec un champ comme un seul objet.

Les propriétés [Start](./get_start/), [Separator](./get_separator/) et [End](./get_end/) pointent respectivement vers les nœuds de début, de séparateur et de fin du champ.

Le contenu entre le début du champ et le séparateur est le code du champ. Le contenu entre le séparateur du champ et la fin du champ est le résultat du champ. Le code du champ se compose généralement d'un ou plusieurs objets [Run](../../aspose.words/run/) qui spécifient des instructions. L'application de traitement doit exécuter le code du champ pour calculer le résultat du champ.

Le processus de calcul des résultats de champ s'appelle la mise à jour du champ. Aspose.Words peut mettre à jour les résultats des champs de la plupart des types de champs exactement de la même manière que Microsoft Word le fait. Notamment, Aspose.Words peut calculer les résultats même des champs de formule les plus complexes. Pour calculer le résultat d'un champ unique, utilisez la méthode [Update](./update/). Pour mettre à jour les champs dans l'ensemble du document, utilisez [UpdateFields](../../aspose.words/document/updatefields/).

Vous pouvez obtenir la version texte brut du code du champ en utilisant la méthode [GetFieldCode()](./getfieldcode/). Vous pouvez obtenir et définir la version texte brut du résultat du champ en utilisant la propriété [Result](./get_result/). Le code du champ et le résultat du champ peuvent tous deux contenir du contenu complexe, tel que des champs imbriqués, des paragraphes, des formes, des tableaux et, dans ce cas, vous pourriez vouloir travailler directement avec les nœuds du champ si vous avez besoin de plus de contrôle.

Vous ne créez pas d'instances de la classe [Field](./) directement. Pour créer un nouveau champ, utilisez la méthode [InsertField()](../).

## Exemples



Montre comment insérer un champ dans un document à l'aide d'un code de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
