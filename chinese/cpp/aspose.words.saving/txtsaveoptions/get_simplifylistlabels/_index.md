---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels 方法"
linktitle: "get_SimplifyListLabels"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels 方法。指定程序是否应在复杂的标签格式无法通过纯文本充分表示时简化列表标签。如果设置为 true，编号列表标签将以简单的数字格式写入，项目符号列表标签则使用简单的 ASCII 字符。默认值在 C++ 中为 false。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


指定程序在纯文本无法充分表示复杂标签格式时是否应简化列表标签。若设置为 **true**，编号列表标签将以简单的数字格式写入，项目符号列表标签则使用简单的 ASCII 字符。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## 示例



展示在将文档保存为纯文本时如何更改列表的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个具有五级缩进的项目符号列表。
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// 创建一个 "TxtSaveOptions" 对象，可将其传递给文档的 "Save" 方法
// 以修改我们保存文档为纯文本的方式。
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// 将 "SimplifyListLabels" 属性设置为 "true" 以转换某些列表
// 符号转换为更简单的 ASCII 字符，例如 '*', 'o', '+', '>', 等。
// 将 "SimplifyListLabels" 属性设置为 "false"，以尽可能保留原始列表符号。
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## 另见

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
