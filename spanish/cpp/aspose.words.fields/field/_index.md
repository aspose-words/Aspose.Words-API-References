---
title: "Aspose::Words::Fields::Field class"
linktitle: "Campo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::Field class. Representa un campo de documento de Microsoft Word. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fields/field/
---
## Field class


Representa un campo de documento de Microsoft Word. Para obtener más información, visite el artículo de documentación.

```cpp
class Field : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](./get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](./get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](./get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](./get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](./get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](./get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](./get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_Result](./get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](./get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](./get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](./get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](./getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](./getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](./update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](./update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Observaciones


Un campo en un documento de Word es una estructura compleja que consta de varios nodos que incluyen inicio de campo, código de campo, separador de campo, resultado de campo y fin de campo. [Fields](../) pueden estar anidados, contener contenido enriquecido y abarcar varios párrafos o secciones en un documento. La clase [Field](./) es un objeto \"facade\" que proporciona propiedades y métodos que permiten trabajar con un campo como un único objeto.

Las propiedades [Start](./get_start/), [Separator](./get_separator/) y [End](./get_end/) apuntan respectivamente a los nodos de inicio, separador y fin del campo.

El contenido entre el inicio del campo y el separador es el código de campo. El contenido entre el separador del campo y el fin del campo es el resultado del campo. El código de campo típicamente consiste en uno o más objetos [Run](../../aspose.words/run/) que especifican instrucciones. Se espera que la aplicación de procesamiento ejecute el código de campo para calcular el resultado del campo.

El proceso de calcular los resultados de los campos se llama actualización de campo. Aspose.Words puede actualizar los resultados de la mayoría de los tipos de campos exactamente de la misma manera que lo hace Microsoft Word. En particular, Aspose.Words puede calcular los resultados incluso de los campos de fórmula más complejos. Para calcular el resultado de un solo campo, use el método [Update](./update/). Para actualizar los campos en todo el documento, use [UpdateFields](../../aspose.words/document/updatefields/).

Puede obtener la versión de texto plano del código de campo usando el método [GetFieldCode()](./getfieldcode/). Puede obtener y establecer la versión de texto plano del resultado del campo usando la propiedad [Result](./get_result/). Tanto el código de campo como el resultado del campo pueden contener contenido complejo, como campos anidados, párrafos, formas, tablas y, en este caso, podría querer trabajar directamente con los nodos del campo si necesita más control.

No crea instancias de la clase [Field](./) directamente. Para crear un nuevo campo use el método [InsertField()](../).

## Ejemplos



Muestra cómo insertar un campo en un documento usando un código de campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
