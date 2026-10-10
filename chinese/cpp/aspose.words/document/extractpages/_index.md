---
title: "Aspose::Words::Document::ExtractPages 方法"
linktitle: "ExtractPages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::ExtractPages 方法。返回表示指定页面范围的 Document 对象（C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


返回表示指定页面范围的 [Document](../) 对象。

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 要提取的第一页的零基索引。 |
| count | int32_t | 要提取的页面数量。 |

## 示例



展示如何从文档中获取指定范围的页面。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


展示如何重置初始页码并保存 NUMPAGE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// 默认行为：
// 提取的页码与原始文档中的相同，就好像我们在 MS Word 中选择了"Print 2 pages"。
// 起始页将被设置为 2，指示页数的字段将被移除
// 并替换为等于页数的常量值。
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// 更改后的行为：
// 提取的页码已重置，并开始新的页码，
// 好像我们已经复制了第二页的内容并粘贴到一个新文档中。
// 起始页将设置为 1，指示页数的字段将保持不变
// 并将显示当前的页数。
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## 另见

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


返回表示指定页面范围以及给定页面提取选项的 [Document](../) 对象。

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 要提取的第一页的零基索引。 |
| count | int32_t | 要提取的页面数量。 |
| options | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | 提供用于管理页面提取过程的选项。 |

## 另见

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
