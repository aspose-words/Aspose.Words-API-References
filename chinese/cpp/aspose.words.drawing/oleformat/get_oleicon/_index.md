---
title: "Aspose::Words::Drawing::OleFormat::get_OleIcon 方法"
linktitle: "get_OleIcon"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat::get_OleIcon 方法。获取 OLE 对象的绘制外观。当为 true 时，OLE 对象显示为图标。当为 false 时，OLE 对象在 C++ 中显示为内容。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing/oleformat/get_oleicon/
---
## OleFormat::get_OleIcon method


获取 OLE 对象的绘制外观。当 **true** 时，OLE 对象显示为图标。当 **false** 时，OLE 对象显示为内容。

```cpp
bool Aspose::Words::Drawing::OleFormat::get_OleIcon()
```

## 备注


Aspose.Words 不允许设置此属性以避免混淆。如果您能够在 Aspose.Words 中更改绘制外观，Microsoft Word 仍会在其原始绘制外观下显示 OLE 对象，直到您在 Microsoft Word 中编辑或更新该 OLE 对象。

## 示例



展示如何插入已链接和未链接的 OLE 对象。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将 Microsoft Visio 绘图嵌入文档中作为 OLE 对象。
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// 插入指向本地文件系统中文件的链接，并将其显示为图标。
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// 插入 OLE 对象会创建存储这些对象的形状。
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// 如果形状包含 OLE 对象，它将具有有效的 "OleFormat" 属性，
// 我们可以使用它来验证形状的某些方面。
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// 如果对象包含 OLE 数据，我们可以使用流来访问它。
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## 另见

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
