---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks 方法"
linktitle: "get_DetectHyperlinks"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks 方法。指定是否在文本中检测超链接。默认值在 C++ 中为 false。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words.loading/txtloadoptions/get_detecthyperlinks/
---
## TxtLoadOptions::get_DetectHyperlinks method


指定是否检测文本中的超链接。默认值为 **false**。

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks() const
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
