---
title: "Clase Aspose::Words::Fields::FieldDisplayBarcode"
linktitle: "FieldDisplayBarcode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldDisplayBarcode. Implementa el campo DISPLAYBARCODE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class


Implementa el campo DISPLAYBARCODE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDisplayBarcode : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Obtiene o establece si se deben agregar caracteres de inicio/fin para los tipos de código de barras NW7 y CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Obtiene o establece el color de fondo del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Obtiene o establece el tipo de código de barras (QR, etc.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Obtiene o establece el valor del código de barras. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_DisplayText](./get_displaytext/)() | Obtiene o establece si se muestra los datos del código de barras (texto) junto con la imagen. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Obtiene o establece el nivel de corrección de errores del código QR. Los valores válidos son [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Obtiene o establece si se corrige el dígito de control cuando es inválido. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Obtiene o establece el color de primer plano del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets or sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_ScalingFactor](./get_scalingfactor/)() | Obtiene o establece un factor de escala para el símbolo. El valor está en puntos porcentuales enteros y los valores válidos son [10, 1000]. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_SymbolHeight](./get_symbolheight/)() | Obtiene o establece la altura del símbolo. Las unidades están en TWIPS (1/1440 de pulgada). |
| [get_SymbolRotation](./get_symbolrotation/)() | Obtiene o establece la rotación del símbolo del código de barras. Los valores válidos son [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_AddStartStopChar](./get_addstartstopchar/). |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_BackgroundColor](./get_backgroundcolor/). |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeType](./get_barcodetype/). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue](./get_barcodevalue/). |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle](./get_casecodestyle/). |
| [set_DisplayText](./set_displaytext/)(bool) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_DisplayText](./get_displaytext/). |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_ErrorCorrectionLevel](./get_errorcorrectionlevel/). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_FixCheckDigit](./get_fixcheckdigit/). |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor](./get_foregroundcolor/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle](./get_poscodestyle/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_ScalingFactor](./get_scalingfactor/). |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight](./get_symbolheight/). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolRotation](./get_symbolrotation/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo insertar un campo DISPLAYBARCODE y establecer sus propiedades.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// A continuación se presentan cuatro tipos de códigos de barras, decorados de diversas maneras, que el campo DISPLAYBARCODE puede mostrar.
// 1 -  Código QR con colores personalizados:
field->set_BarcodeType(u"QR");
field->set_BarcodeValue(u"ABC123");
field->set_BackgroundColor(u"0xF8BD69");
field->set_ForegroundColor(u"0xB5413B");
field->set_ErrorCorrectionLevel(u"3");
field->set_ScalingFactor(u"250");
field->set_SymbolHeight(u"1000");
field->set_SymbolRotation(u"0");

ASSERT_EQ(u" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field->GetFieldCode());
builder->Writeln();

// 2 -  Código de barras EAN13, con los dígitos mostrados debajo de las barras:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  Código CODE39:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  código de barras ITF4, con un código de caso especificado:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
