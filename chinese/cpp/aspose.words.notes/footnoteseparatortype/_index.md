---
title: "Aspose::Words::Notes::FootnoteSeparatorType 枚举"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnoteSeparatorType 枚举。指定了 C++ 中脚注/尾注分隔符的类型。"
type: docs
weight: 6500
url: /zh/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


指定脚注/尾注分隔符的类型。

```cpp
enum class FootnoteSeparatorType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| FootnoteSeparator | 0 | 主文本与脚注文本之间的分隔符。 |
| FootnoteContinuationSeparator | 1 | 当文本必须从前一页继续时，打印在页面上脚注文本上方。 |
| FootnoteContinuationNotice | 2 | 当脚注文本必须在后续页面继续时，打印在页面上脚注文本下方。 |
| EndnoteSeparator | 3 | 主文本与尾注文本之间的分隔符。 |
| EndnoteContinuationSeparator | 4 | 当文本必须从前一页继续时，打印在页面上尾注文本上方。 |
| EndnoteContinuationNotice | 5 | 当尾注文本必须在后续页面继续时，打印在页面上尾注文本下方。 |


## 示例



展示如何移除尾注分隔符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// 移除尾注分隔符。
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


展示如何管理脚注分隔符格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// 对齐脚注分隔符。
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## 另见

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
