---
title: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum"
linktitle: "MailMergeCleanupOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum. Especifica opciones que determinan qué elementos se eliminan durante la combinación de correspondencia en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Especifica opciones que determinan qué elementos se eliminan durante la combinación de correspondencia.

```cpp
enum class MailMergeCleanupOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Especifica un valor predeterminado. |
| RemoveEmptyParagraphs | 1 | Especifica si los párrafos que contenían campos de combinación de correspondencia sin datos deben eliminarse del documento. Cuando esta opción está activada, también se eliminan los párrafos que contienen campos de inicio y fin de región de combinación que están vacíos. |
| RemoveUnusedRegions | 2 | Especifica si las regiones de combinación de correspondencia no utilizadas deben eliminarse del documento. |
| RemoveUnusedFields | 4 | Especifica si los campos de combinación no utilizados deben eliminarse del documento. |
| RemoveContainingFields | 8 | Especifica si los campos que contienen campos de combinación (por ejemplo, IFs) deben eliminarse del documento si los campos de combinación anidados se eliminan. |
| RemoveStaticFields | 16 | Especifica si los campos estáticos deben eliminarse del documento. Los campos estáticos son campos cuyos resultados permanecen iguales ante cualquier cambio del documento. [Fields](../../aspose.words.fields/), que no almacenan sus resultados en un documento y se calculan al vuelo (como [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), etc.) no se consideran estáticos. |
| RemoveEmptyTableRows | 32 | Especifica si las filas vacías que contienen regiones de combinación de correspondencia deben eliminarse del documento. |
| RemoveEmptyTables | 64 | Especifica si se deben eliminar del documento las tablas que contienen regiones de combinación de correspondencia que fueron eliminadas usando la opción [RemoveUnusedRegions](./) o la opción [RemoveEmptyTableRows](./). |

## Ver también

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
