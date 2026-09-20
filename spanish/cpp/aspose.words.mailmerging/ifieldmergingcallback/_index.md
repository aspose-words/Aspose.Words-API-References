---
title: "Interfaz Aspose::Words::MailMerging::IFieldMergingCallback"
linktitle: "IFieldMergingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::MailMerging::IFieldMergingCallback. Implemente esta interfaz si desea controlar cómo se insertan los datos en los campos de combinación durante una operación de combinación de correspondencia en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Implemente esta interfaz si desea controlar cómo se insertan los datos en los campos de combinación durante una operación de combinación de correspondencia.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Se llama cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar datos en un campo de combinación en el documento. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Se llama cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar una imagen en un campo de combinación. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
