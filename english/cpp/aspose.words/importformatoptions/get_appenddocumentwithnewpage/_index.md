---
title: Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage method
linktitle: get_AppendDocumentWithNewPage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage method. Gets or sets a boolean value indicating whether to change a first imported section type to the NewPage forcibly when call AppendDocument(). The default value is true in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Gets or sets a boolean value indicating whether to change a first imported section type to the [NewPage](../../sectionstart/) forcibly when call [AppendDocument()](../). The default value is **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Examples



Shows how to preserve original section type. 
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
