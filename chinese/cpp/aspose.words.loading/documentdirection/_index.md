---
title: "Aspose::Words::Loading::DocumentDirection 枚举"
linktitle: "DocumentDirection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::DocumentDirection 枚举。允许在 C++ 中指定文档中文本的流向方向。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.loading/documentdirection/
---
## DocumentDirection enum


允许指定文档中文本的流向。

```cpp
enum class DocumentDirection
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| LeftToRight | 0 | 从左到右的方向。 |
| RightToLeft | 1 | 从右到左的方向。 |
| 自动 | 2 | 自动检测方向。 |


## 示例



展示如何检测纯文本文档的文本方向。
```cpp
// 创建一个 \"TxtLoadOptions\" 对象，以便我们可以将其传递给文档的构造函数
// 以修改加载纯文本文档的方式。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// 将 \"DocumentDirection\" 属性设置为 \"DocumentDirection.Auto\"，自动检测
// Aspose.Words 从纯文本加载的每个段落的文本方向。
// 每个段落的 \"Bidi\" 属性将存储其方向。
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// 将希伯来文检测为从右到左。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// 将英文检测为从右到左。
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
