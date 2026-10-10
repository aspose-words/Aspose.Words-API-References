---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::FieldMergingArgs class. Proporciona datos para el evento MergeField. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Proporciona datos para el evento **MergeField**. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Devuelve el objeto [Document](../fieldmergingargsbase/get_document/) para el cual se realiza la combinación de correspondencia. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Obtiene el nombre del campo de combinación tal como se especifica en el documento. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Obtiene el objeto que representa el campo de combinación actual. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Obtiene el nombre del campo de combinación en la fuente de datos. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Obtiene el valor del campo de la fuente de datos. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Obtiene el índice basado en cero del registro que se está combinando. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Obtiene el nombre de la tabla de datos para la operación de combinación actual o una cadena vacía si el nombre no está disponible. |
| [get_Text](./get_text/)() const | Obtiene o establece el texto que se insertará en el documento para el campo de combinación actual. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Establece el valor del campo de la fuente de datos. |
| [set_Text](./set_text/)(const System::String\&) | Método set para [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Observaciones


El evento **MergeField** ocurre durante la combinación de correspondencia cuando se encuentra un campo de combinación simple en el documento. Puede responder a este evento para devolver texto que el motor de combinación de correspondencia insertará en el documento.

## Ver también

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
