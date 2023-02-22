---
title: Class FieldAutoNumOut
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldAutoNumOut classe. Implémente le champ AUTONUMOUT.
type: docs
weight: 1450
url: /fr/net/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class

Implémente le champ AUTONUMOUT.

```csharp
public class FieldAutoNumOut : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldAutoNumOut](fieldautonumout/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Insère un numéro automatique au format plan.

### Exemples

Montre comment numéroter des paragraphes à l'aide des champs AUTONUMOUT.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs AUTONUMOUT affichent un nombre qui s'incrémente à chaque champ AUTONUMOUT.
// Contrairement aux champs AUTONUM, les champs AUTONUMOUT utilisent le schéma de numérotation hiérarchique,
// que nous pouvons définir dans Microsoft Word via Format -> Balles & Numérotation -> "Contour numéroté".
// Cela nous permet de numéroter automatiquement les éléments comme une liste numérotée.
// Les champs LISTNUM sont une nouvelle alternative aux champs AUTONUMOUT.
// Ce champ affichera "1.".
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 1.");

// Ce champ affichera "2.".
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 2.");

foreach (FieldAutoNumOut field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumOutline))
    Assert.AreEqual(" AUTONUMOUT ", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUMOUT.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


