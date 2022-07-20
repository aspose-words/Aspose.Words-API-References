---
title: IsUSPostalAddress
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit siPostalAddressaspose.words.fields/fieldbarcode/postaladdress est une adresse postale américaine.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldbarcode/isuspostaladdress/
---
## FieldBarcode.IsUSPostalAddress property

Obtient ou définit si[`PostalAddress`](../postaladdress) est une adresse postale américaine.

```csharp
public bool IsUSPostalAddress { get; set; }
```

### Exemples

Montre comment utiliser le champ CODE-BARRES pour afficher les codes postaux américains sous la forme d'un code-barres.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Vous trouverez ci-dessous deux manières d'utiliser les champs BARCODE pour afficher des valeurs personnalisées sous forme de codes-barres.
// 1 - Stocke la valeur que le code-barres affichera dans la propriété PostalAddress :
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Cette valeur doit être un code postal valide.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Référencez un signet qui stocke la valeur que ce code-barres affichera :
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Le signet auquel le champ BARCODE fait référence dans sa propriété PostalAddress
// ne doit contenir rien d'autre que le code postal valide.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Voir également

* class [FieldBarcode](../../fieldbarcode)
* espace de noms [Aspose.Words.Fields](../../fieldbarcode)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->