---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fields.Field classe. Représente un champ de document Microsoft Word en C#.
type: docs
weight: 1510
url: /fr/net/aspose.words.fields/field/
---
## Field class

Représente un champ de document Microsoft Word.

Pour en savoir plus, visitez le[Travailler avec des champs](https://docs.aspose.com/words/net/working-with-fields/) article documentaire.

```csharp
public class Field
```

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte situé entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/#update)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

## Remarques

Un champ dans un document Word est une structure complexe composée de plusieurs nœuds qui incluent le début du champ, le code de champ , le séparateur de champ, le résultat du champ et la fin du champ. Les champs peuvent être imbriqués, contenir un contenu riche et span plusieurs paragraphes ou sections dans un document. Le`Field` La classe est un objet "façade" qui fournit des propriétés et des méthodes qui permettent de travailler avec un champ comme un objet unique.

Le[`Start`](./start/) ,[`Separator`](./separator/) et[`End`](./end/) Les propriétés pointent respectivement vers les nœuds de début, de séparateur et de fin du champ .

Le contenu entre le début du champ et le séparateur est le code du champ. Le contenu entre le séparateur de champ et la fin du champ est le résultat du champ. Le code de champ se compose généralement d'un ou plusieurs [`Run`](../../aspose.words/run/) objets qui spécifient des instructions. L'application de traitement doit exécuter le code de champ pour calculer le résultat du champ.

Le processus de calcul des résultats sur le terrain est appelé mise à jour du champ. Aspose.Words peut mettre à jour les résultats field de la plupart des types de champs exactement de la même manière que Microsoft Word. Plus particulièrement, Aspose.Words peut calculer les résultats des champs de formule les plus complexes. Pour calculer le résultat field d'un seul champ, utilisez le[`Update`](./update/) méthode. Pour mettre à jour les champs dans l'ensemble du document , utilisez[`UpdateFields`](../../aspose.words/document/updatefields/).

Vous pouvez obtenir la version en texte brut du code du champ en utilisant le[`GetFieldCode`](./getfieldcode/) method. Vous pouvez obtenir et définir la version en texte brut du résultat du champ à l'aide de l'option[`Result`](./result/) property. Le code de champ et le résultat du champ peuvent contenir du contenu complexe, tel que des champs imbriqués, des paragraphes, des formes, des tables et dans ce cas, vous souhaiterez peut-être travailler directement avec les nœuds de champ si vous avez besoin de plus de contrôle.

Vous ne créez pas d'instances de`Field` classe directement. Pour créer un nouveau champ, utilisez le[`InsertField`](../../aspose.words/documentbuilder/insertfield/) méthode.

## Exemples

Montre comment insérer un champ dans un document à l'aide d'un code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
