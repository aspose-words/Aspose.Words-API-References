---
title: "Aspose::Words::Font::get_AllCaps method"
linktitle: "get_AllCaps"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_AllCaps 方法。如果字体被格式化为全大写字母，则为 true（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/font/get_allcaps/
---
## Font::get_AllCaps method


如果字体格式为全大写字母，则为 True。

```cpp
bool Aspose::Words::Font::get_AllCaps()
```


## 示例



展示如何格式化运行以将其内容显示为大写。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// 有两种方法可以让运行在不更改内容的情况下将小写文本显示为大写。
// 1 - 设置 AllCaps 标志以将所有字符显示为常规大写：
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 - 设置 SmallCaps 标志以将所有字符显示为小型大写：
// 如果字符是小写，它将以大写形式显示
// 但高度与小写相同（字体的 x 高度）。
// 原本为大写的字符将保持不变。
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
