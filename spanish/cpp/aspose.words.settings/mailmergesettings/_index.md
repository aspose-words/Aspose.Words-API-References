---
title: "Clase Aspose::Words::Settings::MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Settings::MailMergeSettings. Especifica toda la información de combinación de correspondencia para un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Especifica toda la información de combinación de correspondencia para un documento. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Borra la configuración de combinación de correspondencia de manera que, cuando se guarde el documento, no se guardarán ajustes de combinación y el documento se convertirá en un documento normal. |
| [Clone](./clone/)() | Devuelve una clonación profunda de este objeto. |
| [get_ActiveRecord](./get_activerecord/)() const | Especifica el índice basado en uno del registro de la fuente de datos que se mostrará en Microsoft Word. El valor predeterminado es 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. El valor predeterminado es una cadena vacía. |
| [get_CheckErrors](./get_checkerrors/)() const | Especifica el tipo de informe de errores que Microsoft Word realizará al ejecutar una combinación de correspondencia. El valor predeterminado es [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Especifica la cadena de conexión utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [get_DataSource](./get_datasource/)() const | Especifica la ruta a la fuente de datos de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [get_DataType](./get_datatype/)() const | Especifica el tipo de la fuente de datos de combinación de correspondencia y el método de acceso a los datos. El valor predeterminado es [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Especifica cómo Microsoft Word generará los resultados de una combinación de correspondencia. El valor predeterminado es [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Especifica cómo una aplicación que realiza la combinación de correspondencia debe manejar las líneas en blanco en los documentos combinados resultantes de la combinación. El valor predeterminado es **false**. |
| [get_HeaderSource](./get_headersource/)() const | Especifica la ruta a la fuente de encabezado de la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [get_LinkToQuery](./get_linktoquery/)() const | No estoy seguro sobre este caso. La referencia de automatización de Microsoft Word sugiere que esto indica que la consulta se ejecuta cada vez que el documento se abre en Microsoft Word. Pero la especificación OOXML sugiere que esto indica que la consulta contiene una referencia a un archivo de consulta externo que contiene la consulta real. El valor predeterminado es **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Especifica que los documentos producidos durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar del cuerpo del correo electrónico real. El valor predeterminado es **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Especifica el texto que aparecerá en la línea de asunto de los correos electrónicos o faxes producidos durante la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Especifica el tipo de documento principal de la combinación de correspondencia. El valor predeterminado es [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Obtiene el objeto que especifica la configuración del Office Data Source Object (ODSO). |
| [get_Query](./get_query/)() const | Contiene la cadena de Structured Query Language que se ejecutará contra la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Especifica que Microsoft Word mostrará los datos de la fuente de datos externa especificada donde se hayan insertado campos de combinación (p. ej., vista previa de datos combinados). El valor predeterminado es **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Especifica el índice basado en uno del registro de la fuente de datos que se mostrará en Microsoft Word. El valor predeterminado es 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. El valor predeterminado es una cadena vacía. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Especifica el tipo de informe de errores que Microsoft Word realizará al ejecutar una combinación de correspondencia. El valor predeterminado es [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Especifica la cadena de conexión utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Especifica la ruta a la fuente de datos de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Especifica el tipo de la fuente de datos de combinación de correspondencia y el método de acceso a los datos. El valor predeterminado es [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Especifica cómo Microsoft Word generará los resultados de una combinación de correspondencia. El valor predeterminado es [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Especifica cómo una aplicación que realiza la combinación de correspondencia debe manejar las líneas en blanco en los documentos combinados resultantes de la combinación. El valor predeterminado es **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Especifica la ruta a la fuente de encabezado de la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | Método set para [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Especifica que los documentos producidos durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar del cuerpo del correo electrónico real. El valor predeterminado es **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Especifica el texto que aparecerá en la línea de asunto de los correos electrónicos o faxes producidos durante la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | Método set para [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Establece el objeto que especifica la configuración del Office Data Source Object (ODSO). |
| [set_Query](./set_query/)(const System::String\&) | Contiene la cadena de Structured Query Language que se ejecutará contra la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Especifica que Microsoft Word mostrará los datos de la fuente de datos externa especificada donde se hayan insertado campos de combinación (p. ej., vista previa de datos combinados). El valor predeterminado es **false**. |
| static [Type](./type/)() |  |
## Observaciones


Puede usar este objeto para especificar una fuente de datos de combinación de correspondencia para un documento y esta información (junto con los campos de datos disponibles) aparecerá en Microsoft Word cuando el usuario abra este documento. O puede usar este objeto para consultar la configuración de combinación de correspondencia que el usuario ha especificado en Microsoft Word para este documento.

Normalmente no necesita crear objetos de esta clase directamente porque la configuración de combinación de correspondencia de un documento siempre está disponible a través de la propiedad [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/).

Para detectar si este documento es el documento principal de combinación de correspondencia, verifique el valor de la propiedad [MainDocumentType](./get_maindocumenttype/).

Para eliminar la configuración de combinación de correspondencia y la información de origen de datos de un documento, puede usar el método [Clear](./clear/). Aspose.Words no escribirá la configuración de combinación de correspondencia en un documento si la propiedad [MainDocumentType](./get_maindocumenttype/) está establecida en [NotAMergeDocument](../mailmergemaindocumenttype/) o la propiedad [DataType](./get_datatype/) está establecida en [None](../mailmergedatatype/).

La mejor manera de aprender a usar las propiedades de este objeto es crear un documento con el origen de datos deseado manualmente en Microsoft Word y luego abrir ese documento con Aspose.Words y examinar las propiedades de los objetos [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) y [Odso](./get_odso/). Este es un buen enfoque si desea aprender, por ejemplo, cómo configurar programáticamente un origen de datos.

Aspose.Words conserva la información de combinación de correspondencia al cargar, guardar y convertir documentos entre diferentes formatos, pero no utiliza esta información al realizar su propia combinación de correspondencia usando el objeto [MailMerge](../../aspose.words.mailmerging/mailmerge/).

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
