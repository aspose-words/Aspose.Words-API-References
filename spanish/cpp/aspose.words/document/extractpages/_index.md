---
title: "Método Aspose::Words::Document::ExtractPages"
linktitle: "ExtractPages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::ExtractPages. Devuelve el objeto Document que representa el rango especificado de páginas en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Devuelve el objeto [Document](../) que representa el rango especificado de páginas.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero de la primera página a extraer. |
| count | int32_t | Número de páginas a extraer. |

## Ejemplos



Muestra cómo obtener el rango especificado de páginas del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Devuelve el objeto [Document](../) que representa el rango especificado de páginas y las opciones de extracción de página dadas.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero de la primera página a extraer. |
| count | int32_t | Número de páginas a extraer. |
| opciones | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Proporciona opciones para gestionar el proceso de extracción de páginas. |

## Ver también

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
