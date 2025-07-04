---
title: Aspose::Words::Markup::SdtAppearance enum
linktitle: SdtAppearance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SdtAppearance enum. Specifies the appearance of a structured document tag in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Specifies the appearance of a structured document tag.

```cpp
enum class SdtAppearance
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| BoundingBox | 0 | Represents a structured document tag shown as a shaded rectangle or bounding box. |
| Tags | 1 | Represents a structured document tag shown as start and end markers. |
| Hidden | 2 | Represents a structured document tag that is not shown. |
| Default | n/a | Defaults to [BoundingBox](./). |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
