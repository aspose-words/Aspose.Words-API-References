---
title: "منشئ Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions. يهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
```


## أمثلة



يعرض كيفية قراءة وعرض الروابط التشعبية.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // تحميل المستند مع الروابط التشعبية.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // طباعة نص الروابط التشعبية.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## انظر أيضًا

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
