---
title: FieldAdvance Class
linktitle: FieldAdvance
articleTitle: FieldAdvance
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldAdvance pour une implémentation transparente des champs ADVANCE, améliorant ainsi vos capacités de traitement de documents sans effort.
type: docs
weight: 1950
url: /fr/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Implémente le champ ADVANCE.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldAdvance : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldAdvance](fieldadvance/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset/) { get; set; } | Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé vers le bas. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition/) { get; set; } | Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé horizontalement à partir du bord gauche de la colonne, du cadre ou de la zone de texte. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset/) { get; set; } | Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé vers la gauche. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset/) { get; set; } | Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé vers la droite. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset/) { get; set; } | Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé vers le haut. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition/) { get; set; } | Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé verticalement à partir du bord supérieur de la page. |

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

Déplace le point de départ auquel le texte qui suit lexicalement le champ est affiché vers la droite ou la gauche, vers le haut ou le bas, ou vers une position horizontale ou verticale spécifique.

## Exemples

Montre comment insérer un champ ADVANCE et modifier ses propriétés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Vous trouverez ci-dessous deux manières d'utiliser le champ AVANCE pour ajuster la position du texte qui le suit.
// Les effets d'un champ AVANCE continuent d'être appliqués jusqu'à la fin du paragraphe,
// ou un autre champ ADVANCE met à jour les valeurs de décalage/coordonnées.
// 1 - Spécifiez un décalage directionnel :
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Déplacer le texte vers une position spécifiée par des coordonnées :
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
