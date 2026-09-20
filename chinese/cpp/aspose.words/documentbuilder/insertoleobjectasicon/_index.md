---
title: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon 方法"
linktitle: "InsertOleObjectAsIcon"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon 方法。将嵌入的 OLE 对象作为图标从流插入到文档中。允许指定图标文件和标题。使用给定的 progID 参数在 C++ 中检测 OLE 对象类型。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


从流中将嵌入的 OLE 对象作为图标插入文档中。允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 包含应用程序数据的流。 |
| progId | const System::String\& | OLE 对象的 ProgId。 |
| iconFile | const System::String\& | ICO 文件的完整路径。如果该值为 **null**，Aspose.Words 将使用预定义的图像。 |
| iconCaption | const System::String\& | 图标标题。如果该值为 **null**，Aspose.Words 将使用预定义的图标标题。 |

### ReturnValue

包含 Ole 对象的形状节点，插入到当前 Builder 位置。

## 示例



展示如何将嵌入或链接的 OLE 对象作为图标插入到文档中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果省略了 'iconFile' 和 'iconCaption'，此重载方法将选择
// 根据 'progId' 选择图标，并使用文件名作为图标标题。
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // 如果省略了 'iconFile' 和 'iconCaption'，此重载方法将选择
    // 根据文件扩展名选择图标，并使用文件名作为图标标题。
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


将嵌入或链接的 OLE 对象作为图标插入文档中。允许指定图标文件和标题。使用文件扩展名检测 OLE 对象类型。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文件的完整路径。 |
| isLinked | bool | 如果 **true**，则插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| iconFile | const System::String\& | ICO 文件的完整路径。如果该值为 **null**，Aspose.Words 将使用预定义的图像。 |
| iconCaption | const System::String\& | 图标标题。如果该值为 **null**，Aspose.Words 将使用文件名。 |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


将嵌入或链接的 OLE 对象作为图标插入文档中。允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文件的完整路径。 |
| progId | const System::String\& | OLE 对象的 ProgId。 |
| isLinked | bool | 如果 **true**，则插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| iconFile | const System::String\& | ICO 文件的完整路径。如果该值为 **null**，Aspose.Words 将使用预定义的图像。 |
| iconCaption | const System::String\& | 图标标题。如果该值为 **null**，Aspose.Words 将使用文件名。 |

### ReturnValue

包含 Ole 对象的形状节点，插入到当前 Builder 位置。

## 示例



展示如何将嵌入或链接的 OLE 对象作为图标插入到文档中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果省略了 'iconFile' 和 'iconCaption'，此重载方法将选择
// 根据 'progId' 选择图标，并使用文件名作为图标标题。
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // 如果省略了 'iconFile' 和 'iconCaption'，此重载方法将选择
    // 根据文件扩展名选择图标，并使用文件名作为图标标题。
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
