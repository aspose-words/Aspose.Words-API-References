---
title: Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method
linktitle: get_IgnoreStructuredDocumentTags
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method. Gets or sets a boolean value indicating either to ignore content of StructuredDocumentTag. The default value is false in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/). The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Remarks


When this option is set to **true**, the content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) will be treated as a simple text.

Otherwise, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) will be processed as standalone [Story](../../../aspose.words/story/) and replacing pattern will be searched separately for each [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), so that if pattern crosses a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), then replacement will not be performed for such pattern.

## Examples



Shows how to ignore content of tags from replacement. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// This paragraph contains SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
