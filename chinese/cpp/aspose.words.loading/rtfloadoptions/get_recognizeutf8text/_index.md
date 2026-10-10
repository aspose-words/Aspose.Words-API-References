---
title: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text 方法"
linktitle: "get_RecognizeUtf8Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text 方法。设置为 true 时，将尝试检测 UTF8 字符，这些字符在导入时会被保留，适用于 C++。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


当设置为 **true** 时，将尝试检测 UTF8 字符，并在导入期间保留它们。

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## 备注


默认值为 **false**。

## 示例



展示如何在加载 RTF 文档时检测 UTF-8 字符。
```cpp
// 创建一个 "RtfLoadOptions" 对象，以修改加载 RTF 文档的方式。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// 将 "RecognizeUtf8Text" 属性设置为 "false"，以假设文档使用 ISO 8859-1 字符集
// 并加载文档中的每个字符。
// 将 "RecognizeUtf8Text" 属性设置为 "true"，以解析文本中可能出现的任何可变长度字符。
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## 另见

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
