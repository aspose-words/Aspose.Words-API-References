---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel metod"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel metod. Hämtar eller anger namnet på sekvensidentifieraren som används när en figurförteckning byggs som inte inkluderar bildtextens etikett och nummer i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Hämtar eller anger namnet på sekvensidentifieraren som används när en figurlista byggs som inte inkluderar bildtextens etikett och nummer.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Exempel



Visar hur man anger namnet på sekvensidentifieraren.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## Se även

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
