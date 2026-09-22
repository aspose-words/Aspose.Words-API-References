---
title: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions منشئ"
linktitle: "MarkdownLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions منشئ. يقوم بإنشاء نسخة جديدة من فئة MarkdownLoadOptions في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions::MarkdownLoadOptions constructor


يقوم بإنشاء نسخة جديدة من فئة [MarkdownLoadOptions](../).

```cpp
Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions()
```


## أمثلة



يُظهر كيفية الحفاظ على السطر الفارغ أثناء تحميل المستند.
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

## انظر أيضًا

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
