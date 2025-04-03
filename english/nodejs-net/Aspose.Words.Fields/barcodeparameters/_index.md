---
title: BarcodeParameters class
linktitle: BarcodeParameters class
articleTitle: BarcodeParameters class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.BarcodeParameters class. Container class for barcode parameters to pass-through to BarcodeGenerator"
type: docs
weight: 10
url: /nodejs-net/aspose.words.fields/barcodeparameters/
---

## BarcodeParameters class

Container class for barcode parameters to pass-through to BarcodeGenerator.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Remarks

The set of parameters are according to DISPLAYBARCODE field options.
See the exact list at https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx



### Constructors
| Name | Description |
| --- | --- |
| [BarcodeParameters()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [addStartStopChar](./addStartStopChar/) | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [backgroundColor](./backgroundColor/) | Bar code background color (0x000000 - 0xFFFFFF) |
| [barcodeType](./barcodeType/) | Bar code type. |
| [barcodeValue](./barcodeValue/) | Data to be encoded. |
| [caseCodeStyle](./caseCodeStyle/) | Style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD] |
| [displayText](./displayText/) | Whether to display barcode data (text) along with image. |
| [errorCorrectionLevel](./errorCorrectionLevel/) | Error correction level of QR Code. Valid values are [0, 3]. |
| [facingIdentificationMark](./facingIdentificationMark/) | Type of a Facing Identification Mark (FIM). |
| [fixCheckDigit](./fixCheckDigit/) | Whether to fix the check digit if it’s invalid. |
| [foregroundColor](./foregroundColor/) | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [isBookmark](./isBookmark/) | Whether [BarcodeParameters.postalAddress](./postalAddress/) is the name of a bookmark. |
| [isUSPostalAddress](./isUSPostalAddress/) | Whether [BarcodeParameters.postalAddress](./postalAddress/) is a U.S. postal address. |
| [posCodeStyle](./posCodeStyle/) | Style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [postalAddress](./postalAddress/) | Barcode postal address. |
| [scalingFactor](./scalingFactor/) | Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [symbolHeight](./symbolHeight/) | Bar code image height (in twips - 1/1440 inches) |
| [symbolRotation](./symbolRotation/) | Rotation of the barcode symbol. Valid values are [0, 3]. |

### See Also

* module [Aspose.Words.Fields](../)

