---
title: FieldDisplayBarcode.BackgroundColor
linktitle: BackgroundColor
articleTitle: BackgroundColor
second_title: Aspose.Words pour .NET
description: Personnalisez l'apparence de votre code-barres avec la propriété FieldDisplayBarcode BackgroundColor. Définissez des couleurs vives pour une meilleure visibilité et une meilleure image de marque.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fielddisplaybarcode/backgroundcolor/
---
## FieldDisplayBarcode.BackgroundColor property

Récupère ou définit la couleur d'arrière-plan du symbole du code-barres. Les valeurs valides sont comprises entre [0, 0xFFFFFF]

```csharp
public string BackgroundColor { get; set; }
```

## Exemples

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

// 2 - Code-barres EAN13, avec les chiffres affichés sous les barres :
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - Code-barres CODE39 :
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - Code-barres ITF4, avec un code de cas spécifié :
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Voir également

* class [FieldDisplayBarcode](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
