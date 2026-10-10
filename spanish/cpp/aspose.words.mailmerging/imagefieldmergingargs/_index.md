---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs class. Proporciona datos para el evento ImageFieldMerging(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Proporciona datos para el evento [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/). Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Devuelve el objeto [Document](../fieldmergingargsbase/get_document/) para el cual se realiza la combinación de correspondencia. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Obtiene el nombre del campo de combinación tal como se especifica en el documento. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Obtiene el objeto que representa el campo de combinación actual. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Obtiene el nombre del campo de combinación en la fuente de datos. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Obtiene el valor del campo de la fuente de datos. |
| [get_Image](./get_image/)() const | Especifica la imagen que el motor de combinación de correspondencia debe insertar en el documento. |
| [get_ImageFileName](./get_imagefilename/)() const | Establece el nombre de archivo de la imagen que el motor de combinación de correspondencia debe insertar en el documento. |
| [get_ImageHeight](./get_imageheight/)() const | Especifica la altura de la imagen que se insertará en el documento. |
| [get_ImageStream](./get_imagestream/)() const | Especifica el flujo del que el motor de combinación de correspondencia debe leer una imagen. |
| [get_ImageWidth](./get_imagewidth/)() const | Especifica el ancho de la imagen que se insertará en el documento. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Obtiene el índice basado en cero del registro que se está combinando. |
| [get_Shape](./get_shape/)() const | Especifica la forma que el motor de combinación de correspondencia debe insertar en el documento. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Obtiene el nombre de la tabla de datos para la operación de combinación actual o una cadena vacía si el nombre no está disponible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Establece el valor del campo de la fuente de datos. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Especifica la imagen que el motor de combinación de correspondencia debe insertar en el documento. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Establece el nombre de archivo de la imagen que el motor de combinación de correspondencia debe insertar en el documento. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Método set para [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Especifica el flujo del que el motor de combinación de correspondencia debe leer una imagen. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Método set para [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Método set para [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Observaciones


Este evento ocurre durante la combinación de correspondencia cuando se encuentra un campo de combinación de imagen en el documento. Puede responder a este evento para devolver un nombre de archivo, un flujo o un objeto **Image** al motor de combinación de correspondencia para que se inserte en el documento.

Hay tres propiedades disponibles [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) y [Image](./get_image/) para especificar de dónde se debe obtener la imagen. Establezca solo una de estas propiedades.

Para insertar un campo de combinación de imagen en un documento de Word, seleccione el comando Insertar/Campo, luego seleccione MergeField y escriba Image:MyFieldName.

## Ver también

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
