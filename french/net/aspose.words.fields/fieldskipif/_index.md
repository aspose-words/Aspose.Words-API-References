---
title: Class FieldSkipIf
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldSkipIf classe. Implémente le champ SKIPIF.
type: docs
weight: 2270
url: /fr/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

Implémente le champ SKIPIF.

```csharp
public class FieldSkipIf : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | Obtient ou définit l'opérateur de comparaison. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Obtient ou définit la partie gauche de l'expression de comparaison. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Obtient ou définit la partie droite de l'expression de comparaison. |
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

Compare les valeurs désignées par les expressions[`LeftExpression`](./leftexpression/) et[`RightExpression`](./rightexpression/) en comparaison avec l'opérateur désigné par[`ComparisonOperator`](./comparisonoperator/) Si la comparaison est vraie, SKIPIF annule le document de fusion actuel, passe à l'enregistrement de données suivant dans la source de données et démarre un nouveau document de fusion. Si la comparaison est fausse, le document de fusion actuel se poursuit.

### Exemples

Montre comment ignorer des pages dans un publipostage à l'aide du champ SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ SKIPIF. Si la ligne actuelle d'une opération de fusion et publipostage remplit la condition
// que les expressions de ce champ indiquent, alors l'opération de fusion et publipostage abandonne la ligne en cours,
// supprime le document de fusion actuel, puis passe immédiatement à la ligne suivante pour commencer le document de fusion suivant.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Déplacez le générateur vers le séparateur du champ SKIPIF afin que nous puissions placer un MERGEFIELD à l'intérieur du champ SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// Le MERGEFIELD fait référence à la colonne "Department" dans notre table de données. Si une ligne de cette table
// a une valeur de "HR" dans sa colonne "Department", alors cette ligne remplira la condition.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Ajoutez du contenu à notre document, créez la source de données et exécutez le publipostage.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Cette table a trois lignes, et l'une d'elles remplit la condition de notre champ SKIPIF.
// Le publipostage produira deux pages.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Montre comment utiliser les champs MERGEREC et MERGESEQ pour numéroter et compter les enregistrements de publipostage dans les documents de sortie d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Un champ MERGEREC imprimera le numéro de ligne des données fusionnées dans chaque document de sortie de fusion.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Un champ MERGESEQ comptera le nombre de fusions réussies et imprimera la valeur actuelle sur chaque page respective.
// Si un publipostage n'ignore aucune ligne et n'invoque aucun champ SKIP/SKIPIF/NEXT/NEXTIF, alors toutes les fusions sont réussies.
// Les champs MERGESEQ et MERGEREC afficheront les mêmes résultats si leur publipostage a réussi.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Insère un champ SKIPIF, qui sautera une fusion si le nom est "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Crée une source de données avec 3 lignes, l'une d'elles ayant "John Doe" comme valeur pour la colonne "Name".
// Puisqu'un champ SKIPIF sera déclenché une fois par cette valeur, la sortie de notre publipostage aura 2 pages au lieu de 3.
// Sur la page 1, les champs MERGESEQ et MERGEREC afficheront tous les deux "1".
// Sur la page 2, le champ MERGEREC affichera "3" et le champ MERGESEQ affichera "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


