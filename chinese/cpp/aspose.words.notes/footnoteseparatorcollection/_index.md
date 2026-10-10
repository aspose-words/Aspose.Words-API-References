---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection class"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection class。提供对 C++ 中文档 FootnoteSeparator 节点的类型化访问。"
type: docs
weight: 3667
url: /zh/cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


提供对文档中 [FootnoteSeparator](../footnoteseparator/) 节点的类型化访问。

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | 检索指定类型的 [FootnoteSeparator](../footnoteseparator/)。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



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
