---
title: "Aspose::Words::Saving::MarkdownLinkExportMode enum"
linktitle: "MarkdownLinkExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownLinkExportMode enum. Especifica cómo se exportan los enlaces a Markdown en C++."
type: docs
weight: 67000
url: /es/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Especifica cómo se exportan los enlaces a Markdown.

```cpp
enum class MarkdownLinkExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | 0 | Detectar automáticamente el modo de exportación para cada enlace. |
| En línea | 1 | Exportar todos los enlaces como bloques en línea. |
| Referencia | 2 | Exportar todos los enlaces como bloques de referencia. |


## Ejemplos



Muestra cómo se escribirán los enlaces en el archivo .md.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// La imagen se escribirá como referencia:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// La imagen se escribirá en línea:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
