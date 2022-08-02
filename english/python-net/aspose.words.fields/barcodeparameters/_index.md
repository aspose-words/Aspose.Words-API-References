---
title: BarcodeParameters class
second_title: Aspose.Words for Python via .NET API Reference
description: "Container class for barcode parameters to pass-through to BarcodeGenerator."
type: docs
weight: 10
url: /python-net/aspose.words.fields/barcodeparameters/
---

## BarcodeParameters class

Container class for barcode parameters to pass-through to BarcodeGenerator.


The set of parameters are according to DISPLAYBARCODE field options.
See the exact list at https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx


### Constructors
| Name | Description |
| --- | --- |
| [BarcodeParameters()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [add_start_stop_char](./add_start_stop_char/) | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [background_color](./background_color/) | Bar code background color (0x000000 - 0xFFFFFF) |
| [barcode_type](./barcode_type/) | Bar code type. |
| [barcode_value](./barcode_value/) | Data to be encoded. |
| [case_code_style](./case_code_style/) | Style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD] |
| [display_text](./display_text/) | Whether to display barcode data (text) along with image. |
| [error_correction_level](./error_correction_level/) | Error correction level of QR Code. Valid values are [0, 3]. |
| [facing_identification_mark](./facing_identification_mark/) | Type of a Facing Identification Mark (FIM). |
| [fix_check_digit](./fix_check_digit/) | Whether to fix the check digit if it’s invalid. |
| [foreground_color](./foreground_color/) | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [is_bookmark](./is_bookmark/) | Whether [BarcodeParameters.postal_address](./postal_address/) is the name of a bookmark. |
| [is_us_postal_address](./is_us_postal_address/) | Whether [BarcodeParameters.postal_address](./postal_address/) is a U.S. postal address. |
| [pos_code_style](./pos_code_style/) | Style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [postal_address](./postal_address/) | Barcode postal address. |
| [scaling_factor](./scaling_factor/) | Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [symbol_height](./symbol_height/) | Bar code image height (in twips - 1/1440 inches) |
| [symbol_rotation](./symbol_rotation/) | Rotation of the barcode symbol. Valid values are [0, 3]. |

### See Also

* module [aspose.words.fields](../)

