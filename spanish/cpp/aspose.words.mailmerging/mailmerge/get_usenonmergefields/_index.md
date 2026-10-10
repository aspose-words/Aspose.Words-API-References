---
title: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields method"
linktitle: "get_UseNonMergeFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields method. Cuando es true, especifica que, además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en etiquetas \"{{fieldName}}\" en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.mailmerging/mailmerge/get_usenonmergefields/
---
## MailMerge::get_UseNonMergeFields method


Cuando **true**, especifica que, además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en etiquetas "{{fieldName}}".

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields() const
```

## Observaciones


Normalmente, la combinación de correspondencia solo se realiza en campos MERGEFIELD, pero varios clientes tenían sus informes construidos usando otros campos y generaban muchos documentos de esta manera. Para simplificar la migración (y porque este enfoque fue utilizado de forma independiente por varios clientes) se introdujo la capacidad de combinar correspondencia en otros campos.

Cuando [UseNonMergeFields](./) está configurado a **true**, Aspose.Words realizará la combinación de correspondencia en los siguientes campos:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 \"{FieldName}\" \"\"

Además, cuando [UseNonMergeFields](./) está configurado a **true**, Aspose.Words realizará la combinación de correspondencia en etiquetas de texto \"{{fieldName}}\". Estas no son campos, sino solo etiquetas de texto.
## Ver también

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
