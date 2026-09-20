---
title: "Aspose::Words::Saving::PdfPermissions enum"
linktitle: "PdfPermissions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfPermissions enum. Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado en C++."
type: docs
weight: 80000
url: /es/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado.

```cpp
enum class PdfPermissions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| DisallowAll | 0 | No permite ninguna operación en el documento PDF. Este es el valor predeterminado. |
| AllowAll | 65535 | Permite todas las operaciones en el documento PDF. |
| ContentCopy | n/a | Copiar o extraer de otro modo texto y gráficos del documento mediante operaciones distintas a la controlada por [ContentCopyForAccessibility](./). |
| ContentCopyForAccessibility | n/a | Extraer texto y gráficos (en apoyo a la accesibilidad para usuarios con discapacidades o para otros propósitos). |
| ModifyContents | n/a | Modificar el contenido del documento mediante operaciones distintas a las controladas por [ModifyAnnotations](./), [FillIn](./) y [DocumentAssembly](./). |
| ModifyAnnotations | n/a | Agregar o modificar anotaciones de texto, rellenar campos de formulario interactivos y, si [ModifyContents](./) también está activado, crear o modificar campos de formulario interactivos (incluidos los campos de firma). |
| FillIn | n/a | Rellenar campos de formulario interactivos existentes (incluidos los campos de firma), incluso si [ModifyContents](./) está desactivado. |
| DocumentAssembly | n/a | Ensambla el documento (inserta, rota o elimina páginas y crea elementos de esquema del documento o imágenes en miniatura), incluso si [ModifyContents](./) está desactivado. |
| Printing | n/a | Imprimir el documento (posiblemente no al nivel de mayor calidad, dependiendo de si [HighResolutionPrinting](./) también está activado). |
| HighResolutionPrinting | n/a | Imprimir el documento a una representación a partir de la cual se pueda generar una copia digital fiel del contenido PDF, basada en un algoritmo dependiente de la implementación. Cuando esta bandera está desactivada (y [Printing](./) está activado), la impresión se limitará a una representación de bajo nivel de la apariencia, posiblemente de calidad degradada. |

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
