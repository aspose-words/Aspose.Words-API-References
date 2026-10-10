---
title: "Aspose::Words::Fields::FieldMergeBarcode clase"
linktitle: "FieldMergeBarcode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldMergeBarcode clase. Implementa el campo MERGEBARCODE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 66000
url: /es/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


Implementa el campo MERGEBARCODE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Obtiene si se deben agregar caracteres de inicio/fin para los tipos de código de barras NW7 y CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Obtiene el color de fondo del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Obtiene el tipo de código de barras (QR, etc.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Obtiene el valor del código de barras. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_DisplayText](./get_displaytext/)() | Obtiene si se debe mostrar los datos del código de barras (texto) junto con la imagen. |
| [get_End](./get_end/)() override | Obtiene el nodo que representa el final del campo. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Obtiene un nivel de corrección de errores del código QR. Los valores válidos son [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Obtiene si se debe corregir el dígito de control si es inválido. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Obtiene el color de primer plano del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_ScalingFactor](./get_scalingfactor/)() | Obtiene un factor de escala para el símbolo. El valor está en puntos porcentuales enteros y los valores válidos son [10, 1000]. |
| [get_Separator](./get_separator/)() override | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](./get_start/)() override | Obtiene el nodo que representa el inicio del campo. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_SymbolHeight](./get_symbolheight/)() | Obtiene la altura del símbolo. Las unidades están en TWIPS (1/1440 de pulgada). |
| [get_SymbolRotation](./get_symbolrotation/)() | Obtiene la rotación del símbolo del código de barras. Los valores válidos son [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Establece si se deben agregar caracteres de inicio/fin para los tipos de código de barras NW7 y CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Establece el color de fondo del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Establece el tipo de código de barras (QR, etc.). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Establece el valor del código de barras. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Establece si se deben mostrar los datos del código de barras (texto) junto con la imagen. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Establece un nivel de corrección de errores del código QR. Los valores válidos son [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Establece si se debe corregir el dígito de control si es inválido. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Establece el color de primer plano del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Establece un factor de escala para el símbolo. El valor está en puntos porcentuales enteros y los valores válidos son [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Establece la altura del símbolo. Las unidades están en TWIPS (1/1440 de pulgada). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Establece la rotación del símbolo de código de barras. Los valores válidos son [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
