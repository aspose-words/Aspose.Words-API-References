---
title: "Aspose::Words::Font::get_StyleName 方法"
linktitle: "get_StyleName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_StyleName 方法。获取或设置在 C++ 中应用于此格式的字符样式名称。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words/font/get_stylename/
---
## Font::get_StyleName method


获取或设置应用于此格式的字符样式的名称。

```cpp
System::String Aspose::Words::Font::get_StyleName()
```


## 示例



展示如何更改现有文本的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 下面是引用样式的两种方式。
// 1 -  使用样式名称：
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  使用内置样式标识符：
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// 将一种样式的所有使用转换为另一种样式，
// 使用上述方法引用旧样式和新样式。
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
