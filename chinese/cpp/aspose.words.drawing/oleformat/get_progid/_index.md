---
title: "Aspose::Words::Drawing::OleFormat::get_ProgId 方法"
linktitle: "get_ProgId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat::get_ProgId 方法。获取或设置 C++ 中 OLE 对象的 ProgID。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.drawing/oleformat/get_progid/
---
## OleFormat::get_ProgId method


获取或设置 OLE 对象的 ProgID。

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_ProgId()
```

## 备注


ProgID 属性并非始终存在于 Microsoft Word 文档中，且不能依赖。

不能为 **null**。

默认值为空字符串。

## 示例



展示如何将嵌入的 OLE 对象提取为文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// 第一个形状中的 OLE 对象是 Microsoft Excel 电子表格。
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// 我们的对象既不自动更新，也未锁定更新。
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// 如果我们计划将 OLE 对象保存到本地文件系统中的文件，
// 我们可以使用 "SuggestedExtension" 属性来确定要为文件应用的文件扩展名。
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// 以下是将 OLE 对象保存到本地文件系统中文件的两种方法。
// 1 -  通过流保存它：
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  直接保存到文件名：
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## 另见

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
