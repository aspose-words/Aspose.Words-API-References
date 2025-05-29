---
title: FieldMergeBarcode.ScalingFactor
linktitle: ScalingFactor
articleTitle: ScalingFactor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldMergeBarcode ScalingFactor pour ajuster facilement la taille de votre code-barres en points de pourcentage entiers (10-1000) pour une visibilité optimale.
type: docs
weight: 120
url: /fr/net/aspose.words.fields/fieldmergebarcode/scalingfactor/
---
## FieldMergeBarcode.ScalingFactor property

Obtient ou définit un facteur d'échelle pour le symbole. La valeur est exprimée en points de pourcentage entiers et les valeurs valides sont [10, 1000]

```csharp
public string ScalingFactor { get; set; }
```

## Exemples

Montre comment effectuer un publipostage sur des codes-barres QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un champ MERGEBARCODE, qui acceptera les valeurs d'une source de données lors d'un publipostage.
// Ce champ convertira toutes les valeurs de la colonne « MyQRCode » d'une source de données de fusion en codes QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Appliquer des couleurs et une mise à l'échelle personnalisées.
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

// Créez un DataTable avec une colonne portant le même nom que BarcodeValue de notre champ MERGEBARCODE.
// Le publipostage créera une nouvelle page pour chaque ligne. Chaque page contiendra un champ DISPLAYBARCODE.
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

* class [FieldMergeBarcode](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
