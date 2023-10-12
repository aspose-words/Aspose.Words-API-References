---
title: FieldMergeBarcode.CaseCodeStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldMergeBarcode propriété. Obtient ou définit le style dun code de cas pour le type de codebarres ITF14. Les valeurs valides sont STDEXTADD
type: docs
weight: 60
url: /fr/net/aspose.words.fields/fieldmergebarcode/casecodestyle/
---
## FieldMergeBarcode.CaseCodeStyle property

Obtient ou définit le style d'un code de cas pour le type de code-barres ITF14. Les valeurs valides sont [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

### Exemples

Montre comment effectuer un publipostage sur des codes-barres ITF14.

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

// Créez un DataTable avec une colonne portant le même nom que la BarcodeValue de notre champ MERGEBARCODE.
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

### Voir également

* class [FieldMergeBarcode](../)
* espace de noms [Aspose.Words.Fields](../../fieldmergebarcode/)
* Assemblée [Aspose.Words](../../../)


