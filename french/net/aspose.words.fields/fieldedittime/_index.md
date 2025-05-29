---
title: FieldEditTime Class
linktitle: FieldEditTime
articleTitle: FieldEditTime
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldEditTime pour une édition efficace de vos documents. Simplifiez votre flux de travail grâce à la puissante gestion des champs EDITTIME.
type: docs
weight: 2250
url: /fr/net/aspose.words.fields/fieldedittime/
---
## FieldEditTime class

Implémente le champ EDITTIME.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldEditTime : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldEditTime](fieldedittime/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |

## Remarques

Récupère le temps total d'édition, en minutes, depuis la création du document.

## Exemples

Montre comment utiliser le champ EDITTIME.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le champ EDITTIME affichera, en minutes,
// le temps passé avec le document ouvert dans une fenêtre Microsoft Word.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("You've been editing this document for ");
FieldEditTime field = (FieldEditTime)builder.InsertField(FieldType.FieldEditTime, true);
builder.Writeln(" minutes.");

// Cette propriété de document intégrée enregistre les minutes. Microsoft Word utilise cette propriété.
// pour suivre le temps passé avec le document ouvert. Nous pouvons également le modifier nous-mêmes.
doc.BuiltInDocumentProperties.TotalEditingTime = 10;
field.Update();

Assert.AreEqual(" EDITTIME ", field.GetFieldCode());
Assert.AreEqual("10", field.Result);

// Le champ ne se met pas à jour en temps réel et devra également être
// mis à jour manuellement dans Microsoft Word à chaque fois que nous avons besoin d'une valeur précise.
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.EDITTIME.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
