---
title: "Aspose::Words::Document::Document 构造函数"
linktitle: "Document"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::Document 构造函数。创建一个 C++ 中的空白 Word 文档。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/document/document/
---
## Document::Document() constructor


创建一个空白的 Word 文档。

```cpp
Aspose::Words::Document::Document()
```

## 备注


空白文档从资源中获取，默认情况下，生成的文档看起来更像是由 [Word2007](../../../aspose.words.settings/mswordversion/) 创建的。此空白文档包含默认字体表、最小的默认样式和潜在样式。

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

文档的纸张尺寸默认是 Letter。如果想更改页面设置，请使用 [PageSetup](../../section/get_pagesetup/)。

创建后，您可以使用 [DocumentBuilder](../../documentbuilder/) 轻松添加文档内容。

## 示例



展示如何创建简单文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 新的 Document 对象默认带有最小节点集
// 需要开始添加内容（如文本和形状）：一个 Section、一个 Body 和一个 Paragraph。
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


展示如何创建和加载文档。
```cpp
// 使用 Aspose.Words 创建 Document 对象有两种方式。
// 1 -  创建一个空白文档：
auto doc = System::MakeObject<Aspose::Words::Document>();

// 新的 Document 对象默认带有最小节点集
// 需要开始添加内容（如文本和形状）：一个 Section、一个 Body 和一个 Paragraph。
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  加载本地文件系统中存在的文档：
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// 已加载的文档将包含我们可以访问和编辑的内容。
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// 在加载期间需要执行的一些操作，例如使用密码解密文档，
// 可以在加载文档时传入 LoadOptions 对象来完成。
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


展示如何使用其字体属性格式化文本运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


从流打开现有文档。自动检测文件格式。

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 要从中加载文档的流。 |
## 备注


文档必须存储在流的开头。流必须支持随机定位。

## 示例



展示如何使用流加载文档。
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


从流打开现有文档。允许指定附加选项，例如加密密码。

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 用于加载文档的流。 |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | 加载文档时使用的附加选项。可以为 **null**。 |
## 备注


文档必须存储在流的开头。流必须支持随机定位。

## 示例



展示如何使用基础 URI 从流中打开带有图像的 HTML 文档。
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // 在加载时传递基础文件夹的 URI
    // 以便能够找到 HTML 文档中任何带有相对 URI 的图像。
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // 验证文档的第一个形状包含有效的图像。
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```


展示如何加载加密的 Microsoft Word 文档。
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// 如果尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// 在加载此类文档时，密码通过 LoadOptions 对象传递给文档的构造函数。
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// 使用 LoadOptions 对象加载加密文档有两种方式。
// 1 -  通过文件名从本地文件系统加载文档：
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  从流中加载文档：
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


从文件打开现有文档。自动检测文件格式。

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 要打开的文档文件名。 |

## 示例



展示如何打开文档并将其转换为 .PDF。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


从文件打开现有文档。允许指定附加选项，例如加密密码。

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 要打开的文档文件名。 |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | 加载文档时使用的附加选项。可以为 **null**。 |

## 示例



展示如何创建和加载文档。
```cpp
// 使用 Aspose.Words 创建 Document 对象有两种方式。
// 1 -  创建一个空白文档：
auto doc = System::MakeObject<Aspose::Words::Document>();

// 新的 Document 对象默认带有最小节点集
// 需要开始添加内容（如文本和形状）：一个 Section、一个 Body 和一个 Paragraph。
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  加载本地文件系统中存在的文档：
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// 已加载的文档将包含我们可以访问和编辑的内容。
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// 在加载期间需要执行的一些操作，例如使用密码解密文档，
// 可以在加载文档时传入 LoadOptions 对象来完成。
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


展示如何加载加密的 Microsoft Word 文档。
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// 如果尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// 在加载此类文档时，密码通过 LoadOptions 对象传递给文档的构造函数。
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// 使用 LoadOptions 对象加载加密文档有两种方式。
// 1 -  通过文件名从本地文件系统加载文档：
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  从流中加载文档：
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
