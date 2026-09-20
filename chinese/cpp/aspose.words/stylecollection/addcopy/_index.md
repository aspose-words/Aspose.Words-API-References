---
title: "Aspose::Words::StyleCollection::AddCopy 方法"
linktitle: "AddCopy"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::AddCopy 方法。将在 C++ 中将样式复制到此集合中。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


将样式复制到此集合中。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) 将被复制。 |

### ReturnValue

已复制的样式已准备好使用。
## 备注


[Style](../../style/) to be copied can belong to the same document as well as to different document.

已复制的链接样式。

此方法不会复制基础样式。

如果集合中已存在同名样式，则会自动通过在名称后添加 “_number” 后缀（从 0 开始）生成新名称，例如 “Normal_0”、 “Heading 1_1” 等。使用 [Name](../../style/get_name/) 设置器来更改导入样式的名称。

## 示例



展示如何克隆文档的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// AddCopy 方法创建指定样式的副本，并
// 自动为该样式生成新名称，例如 "Heading 1_0"。
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// 使用样式的 "Name" 属性更改样式的标识名称。
newStyle->set_Name(u"My Heading 1");

// 我们的文档现在有两个外观相同但名称不同的样式。
// 更改其中一个样式的设置不会影响另一个。
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


展示如何将样式从一个文档导入到另一个文档。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// 为源文档创建自定义样式。
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// 将源文档的自定义样式导入到目标文档。
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// 导入的样式外观与其源样式完全相同。
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## 另见

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
