---
title: "Aspose::Words::DocumentBuilder::InsertDocumentInline 方法"
linktitle: "InsertDocumentInline"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertDocumentInline 方法。在 C++ 中于光标位置内联插入文档。"
type: docs
weight: 33500
url: /zh/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


在光标位置内联插入文档。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | 用于插入的源文档。 |
| importFormatMode | Aspose::Words::ImportFormatMode | 指定如何合并冲突的样式格式。 |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | 允许指定影响结果文档格式的选项。 |

### ReturnValue

插入内容的第一个节点。
## 备注


此方法模拟 MS Word 的行为，就好像在一个文档中按下 CTRL+'A'（全选内容），然后按下 CTRL+'C'（将选定内容复制到缓冲区），随后在另一个文档中按下 CTRL+'V'（从缓冲区插入内容）。

与 [InsertDocument()](../) 不同，此方法将目标文档中插入源文档之前的段落内容移动到已插入源文档的最后一个段落中。实际上，这意味着删除了最后插入段落的段落换行符。

注意，如果源文档的最后一个节点不是段落，则不会执行任何操作。

## 示例



展示如何在光标位置内联插入文档。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// 创建目标文档。
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// 将源文档内联插入到目标文档中。
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## 另见

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
