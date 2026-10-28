---
title: Aspose::Words::ImportFormatOptions::set_AppendDocumentWithNewPage method
linktitle: set_AppendDocumentWithNewPage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::set_AppendDocumentWithNewPage method. Sets a boolean value indicating whether to change a first imported section type to the NewPage forcibly when call AppendDocument(). The default value is true in C++.'
type: docs
weight: 12500
url: /cpp/aspose.words/importformatoptions/set_appenddocumentwithnewpage/
---
## ImportFormatOptions::set_AppendDocumentWithNewPage method


Sets a boolean value indicating whether to change a first imported section type to the [NewPage](../../sectionstart/) forcibly when call [AppendDocument()](../../document/appenddocument/). 
The default value is **true**.

```cpp
void Aspose::Words::ImportFormatOptions::set_AppendDocumentWithNewPage(bool value)
```

## Remarks

 Please note that this option is only relevant for the [AppendDocument()](../../document/appenddocument/) method and has no effect on other import-related methods. 
## Examples


Shows how to preserve original section type.

```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```
## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
