---
title: Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml method
linktitle: get_ExportAsHtml
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml method. Allows to specify the elements to be exported to Markdown as raw HTML. Default value is None in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.saving/markdownsaveoptions/get_exportashtml/
---
## MarkdownSaveOptions::get_ExportAsHtml method


Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [None](../../markdownexportashtml/).

```cpp
Aspose::Words::Saving::MarkdownExportAsHtml Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml() const
```


## Examples



Shows how to export a table to Markdown as raw HTML. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Create table.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## See Also

* Enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
