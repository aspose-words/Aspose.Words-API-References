---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName método"
linktitle: "get_FontFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName método. Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la fuente en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la fuente.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Observaciones


Esta propiedad le permite redefinir cómo se generan los nombres de archivo de fuentes durante la exportación a HTML.

Cuando se dispara el evento, esta propiedad contiene el nombre de archivo que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar la fuente en un archivo diferente. Tenga en cuenta que los nombres de archivo deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada fuente incrustada al exportar al formato HTML. Cómo se genera el nombre de archivo de la fuente depende de si guarda el documento en un archivo o en un flujo.

Al guardar un documento en un archivo, el nombre de archivo de fuente generado tiene el aspecto *%<document base file name>.<original file name><optional suffix>.<extension>*.

Al guardar un documento en un flujo, el nombre de archivo de fuente generado tiene el aspecto *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## Ver también

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
