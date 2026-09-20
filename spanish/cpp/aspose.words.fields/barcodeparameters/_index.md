---
title: "Clase Aspose::Words::Fields::BarcodeParameters"
linktitle: "BarcodeParameters"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::BarcodeParameters. Clase contenedora para los parámetros de código de barras que se pasan a BarcodeGenerator. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Clase contenedora para los parámetros de código de barras que se pasan a BarcodeGenerator. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class BarcodeParameters : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Indica si se deben agregar caracteres de inicio/fin para los tipos de código de barras NW7 y CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Color de fondo del código de barras (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Tipo de código de barras. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Datos a codificar. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Si se debe mostrar los datos del código de barras (texto) junto con la imagen. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Nivel de corrección de errores del código QR. Los valores válidos son [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Tipo de una Marca de Identificación Frontal (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Indica si se debe corregir el dígito de control cuando es inválido. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Color de primer plano del código de barras (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Indica si [PostalAddress](./get_postaladdress/) es el nombre de un marcador. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Indica si [PostalAddress](./get_postaladdress/) es una dirección postal de EE. UU. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Dirección postal del código de barras. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Factor de escala para el símbolo. El valor está en puntos porcentuales enteros y los valores válidos son [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Altura de la imagen del código de barras (en twips - 1/1440 pulgadas) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Rotación del símbolo del código de barras. Los valores válidos son [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Indica si se deben agregar caracteres de inicio/fin para los tipos de código de barras NW7 y CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Color de fondo del código de barras (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Tipo de código de barras. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Datos a codificar. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Si se debe mostrar los datos del código de barras (texto) junto con la imagen. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Nivel de corrección de errores del código QR. Los valores válidos son [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Tipo de una Marca de Identificación Frontal (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Indica si se debe corregir el dígito de control cuando es inválido. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Color de primer plano del código de barras (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Indica si [PostalAddress](./get_postaladdress/) es el nombre de un marcador. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Indica si [PostalAddress](./get_postaladdress/) es una dirección postal de EE. UU. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Dirección postal del código de barras. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Factor de escala para el símbolo. El valor está en puntos porcentuales enteros y los valores válidos son [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Altura de la imagen del código de barras (en twips - 1/1440 pulgadas) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Rotación del símbolo del código de barras. Los valores válidos son [0, 3]. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
