---
title: FieldMergeBarcode
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente le champ MERGEBARCODE.
type: docs
weight: 1990
url: /fr/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

Implémente le champ MERGEBARCODE.

```csharp
public class FieldMergeBarcode : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar) { get; set; } | Obtient ou définit s'il faut ajouter des caractères Start/Stop pour les types de codes-barres NW7 et CODE39. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor) { get; set; } | Obtient ou définit la couleur d'arrière-plan du symbole de code-barres. Les valeurs valides sont dans la plage [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype) { get; set; } | Obtient ou définit le type de code-barres (QR, etc.) |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue) { get; set; } | Obtient ou définit la valeur du code-barres. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle) { get; set; } | Obtient ou définit le style d'un code de cas pour le type de code à barres ITF14. Les valeurs valides sont [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext) { get; set; } | Obtient ou définit s'il faut afficher les données de code-barres (texte) avec l'image. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtient le nœud qui représente la fin du champ. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel) { get; set; } | Obtient ou définit un niveau de correction d'erreur de code QR. Les valeurs valides sont [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit) { get; set; } | Obtient ou définit s'il faut corriger le chiffre de contrôle s'il n'est pas valide. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor) { get; set; } | Obtient ou définit la couleur de premier plan du symbole de code-barres. Les valeurs valides sont dans la plage [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtient un[`FieldFormat`](../fieldformat) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtient ou définit le LCID du champ. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle) { get; set; } | Obtient ou définit le style d'un code-barres de point de vente (types de code-barres UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Les valeurs valides (insensibles à la casse) sont [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor) { get; set; } | Obtient ou définit un facteur d'échelle pour le symbole. La valeur est en points de pourcentage entiers et les valeurs valides sont [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtient le nœud qui représente le début du champ. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight) { get; set; } | Obtient ou définit la hauteur du symbole. Les unités sont en TWIPS (1/1440 pouce). |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation) { get; set; } | Obtient ou définit la rotation du symbole de code-barres. Les valeurs valides sont [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Publipostage d'un code-barres.

### Exemples

Montre comment effectuer un publipostage sur les codes-barres ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ MERGEBARCODE, qui acceptera les valeurs d'une source de données lors d'un publipostage.
// Ce champ convertira toutes les valeurs de la colonne "MyITF14Barcode" d'une source de données de fusion en codes-barres ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// Crée un DataTable avec une colonne portant le même nom que la BarcodeValue de notre champ MERGEBARCODE.
// Le publipostage créera une nouvelle page pour chaque ligne. Chaque page contiendra un champ DISPLAYBARCODE,
// qui affichera un code-barres ITF14 avec la valeur de la ligne fusionnée.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

Montre comment effectuer un publipostage sur les codes-barres CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ MERGEBARCODE, qui acceptera les valeurs d'une source de données lors d'un publipostage.
// Ce champ convertira toutes les valeurs de la colonne "MyCODE39Barcode" d'une source de données de fusion en codes-barres CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Modifie son apparence pour afficher les caractères de début/fin.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Crée un DataTable avec une colonne portant le même nom que la BarcodeValue de notre champ MERGEBARCODE.
// Le publipostage créera une nouvelle page pour chaque ligne. Chaque page contiendra un champ DISPLAYBARCODE,
// qui affichera un code-barres CODE39 avec la valeur de la ligne fusionnée.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

Montre comment effectuer un publipostage sur les codes-barres EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ MERGEBARCODE, qui acceptera les valeurs d'une source de données lors d'un publipostage.
// Ce champ convertira toutes les valeurs de la colonne "MyEAN13Barcode" d'une source de données de fusion en codes-barres EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Affiche la valeur numérique du code-barres sous les barres.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Crée un DataTable avec une colonne portant le même nom que la BarcodeValue de notre champ MERGEBARCODE.
// Le publipostage créera une nouvelle page pour chaque ligne. Chaque page contiendra un champ DISPLAYBARCODE,
// qui affichera un code-barres EAN13 avec la valeur de la ligne fusionnée.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

Montre comment effectuer un publipostage sur des codes-barres QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ MERGEBARCODE, qui acceptera les valeurs d'une source de données lors d'un publipostage.
// Ce champ convertira toutes les valeurs de la colonne "MyQRCode" d'une source de données de fusion en codes QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Appliquez des couleurs et une mise à l'échelle personnalisées.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// Crée un DataTable avec une colonne portant le même nom que la BarcodeValue de notre champ MERGEBARCODE.
// Le publipostage créera une nouvelle page pour chaque ligne. Chaque page contiendra un champ DISPLAYBARCODE,
// qui affichera un code QR avec la valeur de la ligne fusionnée.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### Voir également

* class [Field](../field)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
