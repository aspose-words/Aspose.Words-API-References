---
title: "Aspose::Words::Drawing::OleFormat::get_SourceItem 方法"
linktitle: "get_SourceItem"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat::get_SourceItem 方法。获取或设置一个字符串，用于标识在 C++ 中链接的源文件的某一部分。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing/oleformat/get_sourceitem/
---
## OleFormat::get_SourceItem method


获取或设置用于标识正在链接的源文件部分的字符串。

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SourceItem()
```

## 备注


默认值为空字符串。

例如，如果源文件是 Microsoft Excel 工作簿，则 [SourceItem](./) 属性可能返回 "Workbook1!R3C1:R4C2"，前提是 OLE 对象仅包含工作表中的少量单元格。

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
