---
title: FieldBarcode.PostalAddress
linktitle: PostalAddress
articleTitle: PostalAddress
second_title: Aspose.Words for .NET
description: Discover the FieldBarcode PostalAddress property to easily manage postal addresses for barcode generation and bookmark references. Simplify your workflow today!
type: docs
weight: 50
url: /net/aspose.words.fields/fieldbarcode/postaladdress/
---
## FieldBarcode.PostalAddress property

Gets or sets the postal address used for generating a barcode or the name of the bookmark that refers to it.

```csharp
public string PostalAddress { get; set; }
```

## Examples

Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Below are two ways of using BARCODE fields to display custom values as barcodes.
// 1 -  Store the value that the barcode will display in the PostalAddress property:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// This value needs to be a valid ZIP code.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 -  Reference a bookmark that stores the value that this barcode will display:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// The bookmark that the BARCODE field references in its PostalAddress property
// need to contain nothing besides the valid ZIP code.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### See Also

* class [FieldBarcode](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
