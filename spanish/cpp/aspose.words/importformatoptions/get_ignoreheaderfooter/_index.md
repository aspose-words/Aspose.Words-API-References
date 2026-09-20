---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter método"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter método. Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo KeepSourceFormatting. El valor predeterminado es true en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo [KeepSourceFormatting](../../importformatmode/). El valor predeterminado es **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Ejemplos



Muestra cómo especificar la omisión o no del formato de origen del contenido de encabezados/pies de página.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Si 'IgnoreHeaderFooter' es false entonces el formato original del contenido de encabezado/pie de página
// se usará "Header and footer types.docx".
// Si 'IgnoreHeaderFooter' es verdadero, entonces el formato para el contenido de encabezado/pie de página
// se usará "Document.docx".
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
