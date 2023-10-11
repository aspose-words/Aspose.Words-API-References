---
title: FieldDisplayBarcode.CaseCodeStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldDisplayBarcode propriété. Obtient ou définit le style dun code de cas pour le type de codebarres ITF14. Les valeurs valides sont STDEXTADD
type: docs
weight: 60
url: /fr/net/aspose.words.fields/fielddisplaybarcode/casecodestyle/
---
## FieldDisplayBarcode.CaseCodeStyle property

Obtient ou définit le style d'un code de cas pour le type de code-barres ITF14. Les valeurs valides sont [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

### Exemples

Montre comment insérer un champ DISPLAYBARCODE et définir ses propriétés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Vous trouverez ci-dessous quatre types de codes-barres, décorés de différentes manières, que le champ DISPLAYBARCODE peut afficher.
// 1 - QR code avec couleurs personnalisées :
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - Code barre EAN13, avec les chiffres affichés sous les barres :
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - Code barre CODE39 :
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - Code-barres ITF4, avec un code cas spécifié :
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Voir également

* class [FieldDisplayBarcode](../)
* espace de noms [Aspose.Words.Fields](../../fielddisplaybarcode/)
* Assemblée [Aspose.Words](../../../)


