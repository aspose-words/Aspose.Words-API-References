---
title: "Aspose::Words::Drawing::OleFormat 类"
linktitle: "OleFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat 类。提供对 OLE 对象或 ActiveX 控件数据的访问。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


提供对 OLE 对象或 ActiveX 控件数据的访问。要了解更多信息，请访问 [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) 文档文章。

```cpp
class OleFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | 指定在 Microsoft Word 中是否自动更新指向 OLE 对象的链接。 |
| [get_Clsid](./get_clsid/)() | 获取 OLE 对象的 CLSID。 |
| [get_IconCaption](./get_iconcaption/)() | 获取 OLE 对象的图标标题。如果 OLE 对象没有图标或无法检索标题，则返回空字符串。 |
| [get_IsLink](./get_islink/)() | 如果 OLE 对象已链接（当指定了 [SourceFullName](./get_sourcefullname/) 时），返回 **true**。 |
| [get_IsLocked](./get_islocked/)() | 指定链接到 OLE 对象的更新是否被锁定。 |
| [get_OleControl](./get_olecontrol/)() | 如果此 OLE 对象是 ActiveX 控件，则获取 [OleControl](./get_olecontrol/) 对象。否则此属性为 null。 |
| [get_OleIcon](./get_oleicon/)() | 获取 OLE 对象的绘制外观。当 **true** 时，OLE 对象显示为图标。当 **false** 时，OLE 对象显示为内容。 |
| [get_OlePackage](./get_olepackage/)() | 如果 OLE 对象是 OLE 包，则提供对 [OlePackage](../olepackage/) 的访问。否则返回 **null**。 |
| [get_ProgId](./get_progid/)() | 获取或设置 OLE 对象的 ProgID。 |
| [get_SourceFullName](./get_sourcefullname/)() | 获取或设置链接的 OLE 对象的源文件路径和名称。 |
| [get_SourceItem](./get_sourceitem/)() | 获取或设置用于标识正在链接的源文件部分的字符串。 |
| [get_SuggestedExtension](./get_suggestedextension/)() | 获取当前嵌入对象的建议文件扩展名（如果您想将其保存为文件）。 |
| [get_SuggestedFileName](./get_suggestedfilename/)() | 获取当前嵌入对象的建议文件名（如果您想将其保存为文件）。 |
| [GetOleEntry](./getoleentry/)(const System::String\&) | 获取 OLE 对象的数据条目。 |
| [GetRawData](./getrawdata/)() | 获取 OLE 对象的原始数据。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | 将嵌入对象的数据保存到指定的流中。 |
| [Save](./save/)(const System::String\&) | 将嵌入对象的数据保存到具有指定名称的文件中。 |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/) 的设置器。 |
| [set_IsLocked](./set_islocked/)(bool) | [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/) 的设置器。 |
| [set_ProgId](./set_progid/)(const System::String\&) | [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/) 的设置器。 |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/) 的设置器。 |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/) 的设置器。 |
| static [Type](./type/)() |  |
## 备注


使用 [OleFormat](../shape/get_oleformat/) 属性访问 OLE 对象的数据。您不应直接创建 [OleFormat](./) 类的实例。

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
