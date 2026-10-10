---
title: "Aspose::Words::Font::get_Style 方法"
linktitle: "get_Style"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Style 方法。获取或设置在 C++ 中应用于此格式的字符样式。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


获取或设置应用于此格式的字符样式。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## 示例



对文档中使用自定义字符样式格式化的所有运行应用双下划线。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入自定义样式并将其应用于使用文档生成器创建的文本。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// 遍历每个运行，并为每个自定义样式添加双下划线。
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    System::SharedPtr<Aspose::Words::Style> charStyle = run->get_Font()->get_Style();

    if (!charStyle->get_BuiltIn())
    {
        run->get_Font()->set_Underline(Aspose::Words::Underline::Double);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.Style.docx");
```

## 另见

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
