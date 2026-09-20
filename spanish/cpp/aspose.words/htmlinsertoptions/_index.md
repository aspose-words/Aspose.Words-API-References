---
title: "Enumeración Aspose::Words::HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::HtmlInsertOptions enum. Especifica opciones para el método InsertHtml() en C++."
type: docs
weight: 92000
url: /es/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Especifica opciones para el método [InsertHtml()](../).

```cpp
enum class HtmlInsertOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Utilice las opciones predeterminadas al insertar HTML. |
| UseBuilderFormatting | 1 | Utilice el formato de fuente y párrafo especificado en [DocumentBuilder](../documentbuilder/) como formato base para el texto insertado desde HTML. |
| RemoveLastEmptyParagraph | 2 | Elimine el párrafo vacío que normalmente se inserta después de HTML que termina con un elemento de nivel de bloque. |
| PreserveBlocks | 4 | Conserve las propiedades de los elementos de nivel de bloque. |


## Ejemplos



Muestra cómo permite conservar mejor los bordes y márgenes observados.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Establece el nuevo modo de importación de elementos de nivel de bloque HTML.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
