---
title: Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode method
linktitle: get_LinkExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode method. Specifies how links will be written to the output file. Default value is Auto in C++.'
type: docs
weight: 5750
url: /cpp/aspose.words.saving/markdownsaveoptions/get_linkexportmode/
---
## MarkdownSaveOptions::get_LinkExportMode method


Specifies how links will be written to the output file. Default value is [Auto](../../markdownlinkexportmode/).

```cpp
Aspose::Words::Saving::MarkdownLinkExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode() const
```


## Examples



Shows how to links will be written to the .md file. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// Image will be written as reference:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Image will be written as inline:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## See Also

* Enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
