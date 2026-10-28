---
title: Aspose::Words::Fields::FieldToc::set_CaptionlessTableOfFiguresLabel method
linktitle: set_CaptionlessTableOfFiguresLabel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldToc::set_CaptionlessTableOfFiguresLabel method. Sets the name of the sequence identifier used when building a table of figures that does not include caption''s label and number in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words.fields/fieldtoc/set_captionlesstableoffigureslabel/
---
## FieldToc::set_CaptionlessTableOfFiguresLabel method


Sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

```cpp
void Aspose::Words::Fields::FieldToc::set_CaptionlessTableOfFiguresLabel(const System::String & value)
```

## Examples


Shows how to set the name of the sequence identifier.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```
## See Also

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
