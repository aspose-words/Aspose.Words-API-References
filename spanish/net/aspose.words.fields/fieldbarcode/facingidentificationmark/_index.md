---
title: FieldBarcode.FacingIdentificationMark
linktitle: FacingIdentificationMark
articleTitle: FacingIdentificationMark
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldBarcode FacingIdentificationMark para administrar y personalizar fácilmente las marcas de identificación de cara (FIM) para una mayor eficiencia de escaneo.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldbarcode/facingidentificationmark/
---
## FieldBarcode.FacingIdentificationMark property

Obtiene o establece el tipo de una marca de identificación de cara (FIM) para insertar.

```csharp
public string FacingIdentificationMark { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo CÓDIGO DE BARRAS para mostrar códigos postales de EE. UU. en forma de código de barras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// A continuación se muestran dos formas de utilizar los campos CÓDIGO DE BARRAS para mostrar valores personalizados como códigos de barras.
// 1 - Almacena el valor que mostrará el código de barras en la propiedad PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

//Este valor debe ser un código postal válido.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Referencia a un marcador que almacena el valor que mostrará este código de barras:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// El marcador al que hace referencia el campo BARCODE en su propiedad PostalAddress
// no es necesario que contenga nada más que el código postal válido.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Ver también

* class [FieldBarcode](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
