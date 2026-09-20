---
title: "Aspose::Words::DocumentBuilder::PopFont 方法"
linktitle: "PopFont"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::PopFont 方法。检索先前保存在堆栈上的字符格式设置（在 C++ 中）。"
type: docs
weight: 62000
url: /zh/cpp/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder::PopFont method


检索先前保存在堆栈上的字符格式。

```cpp
void Aspose::Words::DocumentBuilder::PopFont()
```


## 示例



展示如何使用文档生成器的格式堆栈。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 设置字体格式，然后编写超链接前的文本。
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// 在堆栈上保留当前的格式配置。
builder->PushFont();

// 通过应用新样式来更改生成器的当前格式。
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// 恢复之前保存的字体格式并从堆栈中移除该元素。
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
