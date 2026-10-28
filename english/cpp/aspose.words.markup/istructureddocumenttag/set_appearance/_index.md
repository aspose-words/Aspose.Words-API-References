---
title: Aspose::Words::Markup::IStructuredDocumentTag::set_Appearance method
linktitle: set_Appearance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::set_Appearance method. Sets the appearance of the structured document tag in C++.'
type: docs
weight: 17750
url: /cpp/aspose.words.markup/istructureddocumenttag/set_appearance/
---
## IStructuredDocumentTag::set_Appearance method


Sets the appearance of the structured document tag.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::set_Appearance(Aspose::Words::Markup::SdtAppearance value)
```

## Examples


Shows how to show tag around content.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Multi-section structured document tags.docx"));
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == SdtAppearance::Hidden)
{
    tag->set_Appearance(SdtAppearance::Tags);
}
```
## See Also

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
