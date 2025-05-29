---
title: FieldSkipIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldSkipIf ComparisonOperator, gérez et personnalisez facilement vos opérateurs de comparaison pour une gestion améliorée des données.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

Obtient ou définit l'opérateur de comparaison.

```csharp
public string ComparisonOperator { get; set; }
```

## Exemples

Montre comment ignorer des pages dans un publipostage à l'aide du champ SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un champ SKIPIF. Si la ligne courante d'une opération de publipostage remplit la condition
// quelles sont les expressions de ce champ, alors l'opération de publipostage annule la ligne actuelle,
// supprime le document de fusion actuel, puis passe immédiatement à la ligne suivante pour commencer le prochain document de fusion.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Déplacez le générateur vers le séparateur du champ SKIPIF afin que nous puissions placer un MERGEFIELD à l'intérieur du champ SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// Le champ MERGEFIELD fait référence à la colonne « Département » de notre table de données. Si une ligne de cette table
// a une valeur de « RH » dans sa colonne « Département », alors cette ligne remplira la condition.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Ajoutez du contenu à notre document, créez la source de données et exécutez le publipostage.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Cette table comporte trois lignes, et l'une d'entre elles remplit la condition de notre champ SKIPIF.
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
// Si un publipostage ne saute aucune ligne et n'appelle aucun champ SKIP/SKIPIF/NEXT/NEXTIF, alors toutes les fusions réussissent.
// Les champs MERGESEQ et MERGEREC afficheront les mêmes résultats si leur fusion a réussi.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Insérez un champ SKIPIF, qui ignorera une fusion si le nom est « John Doe ».
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Créez une source de données avec 3 lignes, l'une d'elles ayant « John Doe » comme valeur pour la colonne « Nom ».
// Étant donné qu'un champ SKIPIF sera déclenché une fois par cette valeur, la sortie de notre publipostage comportera 2 pages au lieu de 3.
// Sur la page 1, les champs MERGESEQ et MERGEREC afficheront tous deux « 1 ».
// Sur la page 2, le champ MERGEREC affichera « 3 » et le champ MERGESEQ affichera « 2 ».
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Voir également

* class [FieldSkipIf](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
