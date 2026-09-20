---
title: "Aspose::Words::Fields::FieldIncludePicture class"
linktitle: "FieldIncludePicture"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldIncludePicture class. Implementa el campo INCLUDEPICTURE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 57000
url: /es/cpp/aspose.words.fields/fieldincludepicture/
---
## FieldIncludePicture class


Implementa el campo INCLUDEPICTURE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIncludePicture : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                            public Aspose::Words::Fields::IFieldIncludePictureCode
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_GraphicFilter](./get_graphicfilter/)() | Obtiene o establece el nombre del filtro para el formato del gráfico que se insertará. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLinked](./get_islinked/)() override | Obtiene o establece si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_ResizeHorizontally](./get_resizehorizontally/)() | Obtiene o establece si se debe redimensionar la imagen horizontalmente desde la fuente. |
| [get_ResizeVertically](./get_resizevertically/)() | Obtiene o establece si se debe redimensionar la imagen verticalmente desde la fuente. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Obtiene o establece la ubicación de la imagen usando un IRI. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_GraphicFilter](./set_graphicfilter/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter](./get_graphicfilter/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Método set para [Aspose::Words::Fields::FieldIncludePicture::get_IsLinked](./get_islinked/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResizeHorizontally](./set_resizehorizontally/)(bool) | Método set para [Aspose::Words::Fields::FieldIncludePicture::get_ResizeHorizontally](./get_resizehorizontally/). |
| [set_ResizeVertically](./set_resizevertically/)(bool) | Método set para [Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically](./get_resizevertically/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldIncludePicture::get_SourceFullName](./get_sourcefullname/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo insertar imágenes usando los campos IMPORT e INCLUDEPICTURE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de campo similares que podemos usar para mostrar imágenes enlazadas desde el sistema de archivos local.
// 1 -  El campo INCLUDEPICTURE:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Aplicar el filtro PNG32.FLT.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  El campo IMPORT:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
