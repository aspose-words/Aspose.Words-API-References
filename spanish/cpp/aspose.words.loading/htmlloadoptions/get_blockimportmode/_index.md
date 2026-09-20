---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode método"
linktitle: "get_BlockImportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode método. Obtiene o establece un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor predeterminado es Merge en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


Obtiene o establece un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor predeterminado es [Merge](../../blockimportmode/).

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


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

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
