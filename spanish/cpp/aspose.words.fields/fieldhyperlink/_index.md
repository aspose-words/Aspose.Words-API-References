---
title: "Aspose::Words::Fields::FieldHyperlink class"
linktitle: "FieldHyperlink"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldHyperlink class. Implementa el campo HYPERLINK. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 53000
url: /es/cpp/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class


Implementa el campo HYPERLINK. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldHyperlink : public Aspose::Words::Fields::Field,
                       public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                       public Aspose::Words::Fields::IFieldResultFormatProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Address](./get_address/)() | Obtiene o establece una ubicación a la que este hipervínculo salta. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsImageMap](./get_isimagemap/)() | Obtiene o establece si se deben agregar coordenadas al hipervínculo para un mapa de imágenes del lado del servidor. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_OpenInNewWindow](./get_openinnewwindow/)() | Obtiene o establece si se debe abrir el sitio de destino en una nueva ventana del navegador web. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_ScreenTip](./get_screentip/)() | Obtiene o establece el texto de ScreenTip para el hipervínculo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_SubAddress](./get_subaddress/)() | Obtiene o establece una ubicación en el archivo, como un marcador, a la que este hipervínculo salta. |
| [get_Target](./get_target/)() | Obtiene o establece el objetivo al que debe redirigirse el enlace. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_Address](./set_address/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldHyperlink::get_Address](./get_address/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsImageMap](./set_isimagemap/)(bool) | Método set para [Aspose::Words::Fields::FieldHyperlink::get_IsImageMap](./get_isimagemap/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_OpenInNewWindow](./set_openinnewwindow/)(bool) | Método set para [Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow](./get_openinnewwindow/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldHyperlink::get_ScreenTip](./get_screentip/). |
| [set_SubAddress](./set_subaddress/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldHyperlink::get_SubAddress](./get_subaddress/). |
| [set_Target](./set_target/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldHyperlink::get_Target](./get_target/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo usar campos HYPERLINK para enlazar a documentos en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Cuando hacemos clic en este campo HYPERLINK en Microsoft Word,
// abrirá el documento vinculado y luego colocará el cursor en el marcador especificado.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Cuando hacemos clic en este campo HYPERLINK en Microsoft Word,
// abrirá el documento vinculado y se desplazará automáticamente hacia abajo hasta el iframe especificado.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
