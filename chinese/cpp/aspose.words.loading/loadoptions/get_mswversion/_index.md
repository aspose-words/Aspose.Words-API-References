---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion 方法"
linktitle: "get_MswVersion"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion 方法。允许指定文档加载过程应匹配特定的 MS Word 版本。默认值在 C++ 中为 Word2019。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


允许指定文档加载过程应匹配特定的 MS Word 版本。默认值为 [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## 示例



展示如何在文档加载期间模拟特定 Microsoft Word 版本的加载过程。
```cpp
// 默认情况下，Aspose.Words 按照 Microsoft Word 2019 规范加载文档。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// 此文档缺少默认段落格式样式。
// 当我们使用 Microsoft Word 或 Aspose.Words 加载文档时，将重新生成此默认样式。
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// 当按照 Microsoft Word 2007 规范加载时，样式的行间距将具有此值。
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## 另见

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
