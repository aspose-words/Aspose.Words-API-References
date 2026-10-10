---
title: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName método"
linktitle: "get_DocumentFieldName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName método. Obtiene el nombre del campo de combinación tal como se especifica en el documento en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.mailmerging/fieldmergingargsbase/get_documentfieldname/
---
## FieldMergingArgsBase::get_DocumentFieldName method


Obtiene el nombre del campo de combinación tal como se especifica en el documento.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName() const
```

## Observaciones


Si tiene un mapeo de un nombre de campo del documento a un nombre de campo de origen de datos diferente, entonces este es el nombre de campo original tal como se especifica en el documento.

Si especificó un prefijo de nombre de campo, por ejemplo \"Image:MyFieldName\" en el documento, entonces [DocumentFieldName](./) devuelve el nombre del campo sin el prefijo, que es \"MyFieldName\".
## Ver también

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
