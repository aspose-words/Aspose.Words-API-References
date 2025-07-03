---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance method
linktitle: get_Appearance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance method. Gets or sets the appearance of the structured document tag in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_appearance/
---
## StructuredDocumentTagRangeStart::get_Appearance method


Gets or sets the appearance of the structured document tag.

```cpp
Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance() override
```


## Examples



Shows how to show tag around content. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## See Also

* Enum [SdtAppearance](../../sdtappearance/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
