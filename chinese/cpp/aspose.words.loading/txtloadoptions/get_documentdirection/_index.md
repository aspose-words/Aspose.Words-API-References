---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection 方法"
linktitle: "get_DocumentDirection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection 方法。获取或设置文档方向。默认值为 LeftToRight，在 C++ 中。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


获取或设置文档方向。默认值为 [LeftToRight](../../documentdirection/)。

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


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

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
