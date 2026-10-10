---
title: "Aspose::Words::PageExtractOptions clase"
linktitle: "PageExtractOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::PageExtractOptions. Permite especificar opciones para la extracción de páginas de documentos en C++."
type: docs
weight: 45500
url: /es/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


Permite especificar opciones para la extracción de páginas del documento.

```cpp
class PageExtractOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | Especifica si los campos NUMPAGES en el documento resultante serán reemplazados por sus valores reales. El valor predeterminado es **true**. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | Especifica si el número de página inicial en el documento resultante se actualizará. El valor predeterminado es **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | Método setter para [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | Método setter para [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo restablecer la numeración de página inicial y guardar el campo NUMPAGE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Comportamiento predeterminado:
// La numeración de página extraída es la misma que en el documento original, como si hubiéramos seleccionado "Imprimir 2 páginas" en MS Word.
// La página de inicio se establecerá en 2 y el campo que indica el número de páginas será eliminado
// y reemplazado por un valor constante igual al número de páginas.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Comportamiento alterado:
// La numeración de página extraída se restablece y comienza una nueva,
// como si hubiéramos copiado el contenido de la segunda página y lo pegado en un nuevo documento.
// La página de inicio se establecerá en 1 y el campo que indica el número de páginas permanecerá sin cambios
// y mostrará el número actual de páginas.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
