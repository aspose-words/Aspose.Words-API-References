---
title: Aspose::Words::Loading::MarkdownLoadOptions::set_PreserveEmptyLines method
linktitle: set_PreserveEmptyLines
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::MarkdownLoadOptions::set_PreserveEmptyLines method. Sets a boolean value indicating whether to preserve empty lines while load a Markdown document. The default value is false.  Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and end of the document are also ignored. This option allows to import such empty lines in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.loading/markdownloadoptions/set_preserveemptylines/
---
## MarkdownLoadOptions::set_PreserveEmptyLines method


Sets a boolean value indicating whether to preserve empty lines while load a [Markdown](../../../aspose.words/loadformat/) document. The default value is **false**. 
 Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and end of the document are also ignored. This option allows to import such empty lines.

```cpp
void Aspose::Words::Loading::MarkdownLoadOptions::set_PreserveEmptyLines(bool value)
```

## Examples


Shows how to preserve empty line while load a document.

```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```
## See Also

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
