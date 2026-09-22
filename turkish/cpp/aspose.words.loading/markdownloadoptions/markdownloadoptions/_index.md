---
title: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions yapıcı"
linktitle: "MarkdownLoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions yapıcı. C++'ta MarkdownLoadOptions sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions::MarkdownLoadOptions constructor


Yeni bir [MarkdownLoadOptions](../) sınıf örneği başlatır.

```cpp
Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions()
```


## Örnekler



Bir belge yüklenirken boş satırın nasıl korunacağını gösterir.
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

## Ayrıca Bakınız

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
