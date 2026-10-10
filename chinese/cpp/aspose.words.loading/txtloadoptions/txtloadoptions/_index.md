---
title: "Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions 构造函数"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions 构造函数。使用默认值在 C++ 中初始化此类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions::TxtLoadOptions constructor


使用默认值初始化此类的新实例。

```cpp
Aspose::Words::Loading::TxtLoadOptions::TxtLoadOptions()
```


## 示例



展示如何读取和显示超链接。
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // 加载包含超链接的文档。
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // 打印超链接文本。
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## 另见

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
