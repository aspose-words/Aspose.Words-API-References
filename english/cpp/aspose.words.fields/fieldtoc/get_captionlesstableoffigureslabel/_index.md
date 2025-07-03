---
title: Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel method
linktitle: get_CaptionlessTableOfFiguresLabel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel method. Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption''s label and number in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Examples



Shows how to set the name of the sequence identifier. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## See Also

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
