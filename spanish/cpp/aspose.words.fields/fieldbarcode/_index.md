---
title: "Clase Aspose::Words::Fields::FieldBarcode"
linktitle: "FieldBarcode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldBarcode. Implementa el campo BARCODE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class


Implementa el campo BARCODE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldBarcode : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() | Obtiene o establece el tipo de una Marca de Identificación Frontal (FIM) para insertar. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsBookmark](./get_isbookmark/)() | Obtiene o establece si [PostalAddress](./get_postaladdress/) es el nombre de un marcador. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() | Obtiene o establece si [PostalAddress](./get_postaladdress/) es una dirección postal de EE. UU. |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PostalAddress](./get_postaladdress/)() | Obtiene o establece la dirección postal utilizada para generar un código de barras o el nombre del marcador que la referencia. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark](./get_facingidentificationmark/). |
| [set_IsBookmark](./set_isbookmark/)(bool) | Método set para [Aspose::Words::Fields::FieldBarcode::get_IsBookmark](./get_isbookmark/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Método set para [Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress](./get_isuspostaladdress/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldBarcode::get_PostalAddress](./get_postaladdress/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo usar el campo BARCODE para mostrar códigos ZIP de EE. UU. en forma de código de barras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// A continuación se presentan dos formas de usar campos BARCODE para mostrar valores personalizados como códigos de barras.
// 1 -  Almacene el valor que el código de barras mostrará en la propiedad PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Este valor debe ser un código postal válido.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Referencie un marcador que almacene el valor que este código de barras mostrará:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// El marcador que el campo BARCODE referencia en su propiedad PostalAddress
// debe contener únicamente el código postal válido.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
