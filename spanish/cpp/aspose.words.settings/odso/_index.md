---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::Odso class. Especifica la configuración del Office Data Source Object (ODSO) para una fuente de datos de combinación de correspondencia. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.settings/odso/
---
## Odso class


Especifica la configuración del Objeto de Fuente de Datos de Office (ODSO) para una fuente de datos de combinación de correspondencia. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Devuelve una clonación profunda de este objeto. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Especifica el carácter que se interpretará como delimitador de columna utilizado para separar columnas dentro de fuentes de datos externas. El valor predeterminado es 0, lo que significa que no hay delimitador de columna definido. |
| [get_DataSource](./get_datasource/)() const | Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [get_DataSourceType](./get_datasourcetype/)() const | Especifica el tipo de la fuente de datos externa que se conectará como parte de la información de conexión ODSO para esta combinación de correspondencia. El valor predeterminado es [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Obtiene una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campo de combinación predefinidos en el documento. Este objeto nunca es **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Especifica que una aplicación anfitriona debe tratar la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. El valor predeterminado es **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Obtiene una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nunca es **null**. |
| [get_TableName](./get_tablename/)() const | Especifica el conjunto particular de datos al que una fuente debe conectarse dentro de una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Especifica la cadena de conexión Universal Data Link (UDL) utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Método setter para [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Método setter para [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Establece una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campos de combinación predefinidos en el documento. Este objeto nunca es **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Método setter para [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Establece una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nunca es **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | Especifica el conjunto particular de datos al que una fuente debe conectarse dentro de una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Especifica la cadena de conexión Universal Data Link (UDL) utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| static [Type](./type/)() |  |
## Observaciones


ODSO parece ser la forma "nueva" que las versiones más recientes de Microsoft Word prefieren usar al especificar ciertos tipos de fuentes de datos para un documento de combinación de correspondencia. ODSO probablemente apareció por primera vez en Microsoft Word 2000.

El uso de ODSO está pobremente documentado y la mejor manera de aprender a usar las propiedades de este objeto es crear un documento con la fuente de datos deseada manualmente en Microsoft Word y luego abrir ese documento usando Aspose.Words y examinar las propiedades de los objetos [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) y [Odso](../mailmergesettings/get_odso/). Este es un buen enfoque si deseas aprender a configurar programáticamente una fuente de datos, por ejemplo.

Normalmente no necesitas crear objetos de esta clase directamente porque la configuración de ODSO siempre está disponible a través de la propiedad [Odso](../mailmergesettings/get_odso/).

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
