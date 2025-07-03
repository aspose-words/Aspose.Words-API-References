---
title: Aspose::Words::BaselineAlignment enum
linktitle: BaselineAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BaselineAlignment enum. Specifies fonts vertical position on a line in C++.'
type: docs
weight: 80500
url: /cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Specifies fonts vertical position on a line.

```cpp
enum class BaselineAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Top | 0 | Aligns along the top of each font. |
| Center | 1 | Aligns the center points of each font. |
| Baseline | 2 | Aligns to the baseline of the paragraph. |
| Bottom | 3 | Aligns to the bottom of each font. |
| Auto | 4 | Baseline is adjusted automatically. |


## Examples



Shows how to set fonts vertical position on a line. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
