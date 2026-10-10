---
title: "Aspose::Words::Settings::OdsoFieldMapData clase"
linktitle: "OdsoFieldMapData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Settings::OdsoFieldMapData. Especifica cómo se debe mapear una columna en la fuente de datos externa a los campos de combinación predefinidos dentro del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Especifica cómo se debe mapear una columna de la fuente de datos externa a los campos de combinación predefinidos dentro del documento. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Devuelve una clonación profunda de este objeto. |
| [get_Column](./get_column/)() const | Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se debe mapear al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0. |
| [get_MappedName](./get_mappedname/)() const | Especifica el nombre del campo de combinación predefinido que se debe mapear al número de columna especificado por la propiedad [Column](./get_column/) dentro de este mapeo de campos. El valor predeterminado es una cadena vacía. |
| [get_Name](./get_name/)() const | Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por la propiedad [Column](./get_column/). El valor predeterminado es una cadena vacía. |
| [get_Type](./get_type/)() const | Especifica si un campo de combinación de correo dado ha sido mapeado a una columna en la fuente de datos externa correspondiente o no. El valor predeterminado es [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se debe mapear al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Especifica el nombre del campo de combinación predefinido que se debe mapear al número de columna especificado por la propiedad [Column](./get_column/) dentro de este mapeo de campos. El valor predeterminado es una cadena vacía. |
| [set_Name](./set_name/)(const System::String\&) | Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por la propiedad [Column](./get_column/). El valor predeterminado es una cadena vacía. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Especifica si un campo de combinación de correo dado ha sido mapeado a una columna en la fuente de datos externa correspondiente o no. El valor predeterminado es [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Observaciones


Microsoft Word proporciona algunos nombres de campos de combinación predefinidos que permite insertar en un documento como MERGEFIELD o usar en los campos ADDRESSBLOCK o GREETINGLINE. La información especificada en [OdsoFieldMapData](./) permite mapear una columna en la fuente de datos externa a un solo campo de combinación predefinido.

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
