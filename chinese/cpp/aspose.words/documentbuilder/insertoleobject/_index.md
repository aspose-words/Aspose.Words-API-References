---
title: "Aspose::Words::DocumentBuilder::InsertOleObject 方法"
linktitle: "InsertOleObject"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertOleObject 方法。从流中插入嵌入的 OLE 对象到文档中（C++）。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


从流中插入嵌入的 OLE 对象到文档中。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 包含应用程序数据的流。 |
| progId | const System::String\& | OLE 对象的编程标识符。 |
| asIcon | bool | 指定要插入的 OLE 对象的 Iconic 或 Normal 模式。 |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | OLE 对象的图像呈现方式。如果值为 **null**，Aspose.Words 将使用预定义的图像之一。 |

### ReturnValue

包含 Ole 对象的形状节点，插入到当前 Builder 位置。

## 示例



展示如何使用文档生成器在文档中嵌入 OLE 对象。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个来自本地文件系统的 Microsoft Excel 电子表格
// 将其插入文档，同时保持默认外观。
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
    // 根据 'progId' 的图标，并使用预定义的图标标题。
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// 将 Microsoft Powerpoint 演示文稿作为 OLE 对象插入。
// 这次，它将使用从网络下载的图像作为图标。
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// 在 Microsoft Word 中双击这些对象以打开
// 使用各自的应用程序打开链接的文件。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


从文件中插入嵌入或链接的 OLE 对象到文档中。使用文件扩展名检测 OLE 对象类型。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文件的完整路径。 |
| isLinked | bool | 如果 **true**，则插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| asIcon | bool | 指定要插入的 OLE 对象的 Iconic 或 Normal 模式。 |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | OLE 对象的图像呈现方式。如果值为 **null**，Aspose.Words 将使用预定义的图像之一。 |

### ReturnValue

包含 Ole 对象的形状节点，插入到当前 Builder 位置。

## 示例



展示如何在文档中插入 OLE 对象。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE 对象是指向本地文件系统中文件的链接，可由其他已安装的应用程序打开。
// 双击这些形状将启动相应的应用程序，然后使用它打开链接的对象。
// 使用 InsertOleObject 方法插入这些形状并配置其外观有三种方式。
// 1 - 来自本地文件系统的图像：
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
    // 根据文件扩展名选择图标，并使用文件名作为图标标题。
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
// 根据 'progId' 选择图标，并使用文件名作为图标标题。
// 2 - 基于将打开对象的应用程序的图标：
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// 如果省略了 'iconFile' 和 'iconCaption'，此重载方法将选择
// 根据 'progId' 的图标，并使用预定义的图标标题。
// 3 - 来自本地文件系统、尺寸为 32 x 32 像素或更小的图像图标，并带有自定义标题：
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


从文件中插入嵌入或链接的 OLE 对象到文档中。使用给定的 progID 参数检测 OLE 对象类型。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文件的完整路径。 |
| progId | const System::String\& | OLE 对象的 ProgId。 |
| isLinked | bool | 如果 **true**，则插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| asIcon | bool | 指定要插入的 OLE 对象的 Iconic 或 Normal 模式。 |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | OLE 对象的图像呈现方式。如果值为 **null**，Aspose.Words 将使用预定义的图像之一。 |

### ReturnValue

包含 Ole 对象的形状节点，插入到当前 Builder 位置。

## 示例



展示如何在文档中插入 OLE 对象。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE 对象是指向本地文件系统中文件的链接，可由其他已安装的应用程序打开。
// 双击这些形状将启动相应的应用程序，然后使用它打开链接的对象。
// 使用 InsertOleObject 方法插入这些形状并配置其外观有三种方式。
// 1 - 来自本地文件系统的图像：
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
    // 根据文件扩展名选择图标，并使用文件名作为图标标题。
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
// 根据 'progId' 选择图标，并使用文件名作为图标标题。
// 2 - 基于将打开对象的应用程序的图标：
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// 如果省略了 'iconFile' 和 'iconCaption'，此重载方法将选择
// 根据 'progId' 的图标，并使用预定义的图标标题。
// 3 - 来自本地文件系统、尺寸为 32 x 32 像素或更小的图像图标，并带有自定义标题：
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
