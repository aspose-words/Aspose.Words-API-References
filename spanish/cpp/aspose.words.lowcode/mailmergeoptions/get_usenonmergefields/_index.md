---
title: "Método Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields"
linktitle: "get_UseNonMergeFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields. Cuando true, especifica que, además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en etiquetas \\\"{{fieldName}}\\\" en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


Cuando **true**, especifica que, además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en etiquetas "{{fieldName}}".

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## Observaciones


Normalmente, la combinación de correspondencia solo se realiza en campos MERGEFIELD, pero varios clientes tenían sus informes construidos usando otros campos y generaban muchos documentos de esta manera. Para simplificar la migración (y porque este enfoque fue utilizado de forma independiente por varios clientes) se introdujo la capacidad de combinar correspondencia en otros campos.

Cuando [UseNonMergeFields](./) está configurado a **true**, Aspose.Words realizará la combinación de correspondencia en los siguientes campos:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 \"{FieldName}\" \"\"

Además, cuando [UseNonMergeFields](./) está configurado a **true**, Aspose.Words realizará la combinación de correspondencia en etiquetas de texto \"{{fieldName}}\". Estas no son campos, sino solo etiquetas de texto.
## Ver también

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
