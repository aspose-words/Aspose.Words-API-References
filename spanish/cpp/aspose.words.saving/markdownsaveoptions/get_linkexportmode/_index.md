---
title: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode"
linktitle: "get_LinkExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode. Especifica cómo se escribirán los enlaces en el archivo de salida. El valor predeterminado es Auto en C++."
type: docs
weight: 5750
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_linkexportmode/
---
## MarkdownSaveOptions::get_LinkExportMode method


Especifica cómo se escribirán los enlaces en el archivo de salida. El valor predeterminado es [Auto](../../markdownlinkexportmode/).

```cpp
Aspose::Words::Saving::MarkdownLinkExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode() const
```


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

* Enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
