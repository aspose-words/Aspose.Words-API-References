---
title: "طريقة Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines"
linktitle: "get_PreserveEmptyLines"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب الحفاظ على الأسطر الفارغة أثناء تحميل مستند Markdown. القيمة الافتراضية هي false. عادةً، يتم تجاهل الأسطر الفارغة بين العناصر ذات المستوى الكتلي في Markdown. كما يتم تجاهل الأسطر الفارغة في بداية ونهاية المستند. يتيح هذا الخيار استيراد هذه الأسطر الفارغة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب الحفاظ على الأسطر الفارغة أثناء تحميل مستند [Markdown](../../../aspose.words/loadformat/). القيمة الافتراضية هي **false**. عادةً، يتم تجاهل الأسطر الفارغة بين العناصر ذات المستوى الكتلي في Markdown. كما يتم تجاهل الأسطر الفارغة في بداية ونهاية المستند. يتيح هذا الخيار استيراد هذه الأسطر الفارغة.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
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
