---
title: Aspose::Words::Saving::MarkdownLinkExportMode enum
linktitle: MarkdownLinkExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownLinkExportMode enum. Specifies how links are exported into Markdown in C++.'
type: docs
weight: 67000
url: /cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Specifies how links are exported into Markdown.

```cpp
enum class MarkdownLinkExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 0 | Automatically detect export mode for each link. |
| Inline | 1 | Export all links as inline blocks. |
| Reference | 2 | Export all links as reference blocks. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
