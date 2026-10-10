---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::BlockImportMode enum. Especifica cómo se importan las propiedades de los elementos de nivel de bloque desde documentos basados en HTML en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Especifica cómo se importan las propiedades de los elementos de nivel de bloque desde documentos basados en HTML.

```cpp
enum class BlockImportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) de los bloques padre se fusionan y se almacenan en los elementos hijo (p. ej., párrafos o tablas). |
| Preserve | 1 | [Properties](../../aspose.words.properties/) de los bloques padre se importan a una estructura lógica especial y se almacenan por separado de los nodos del documento. |


## Ejemplos



Muestra cómo se importan las propiedades de los elementos de nivel de bloque desde documentos basados en HTML.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Establece el nuevo modo de importación de elementos de nivel de bloque HTML.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
