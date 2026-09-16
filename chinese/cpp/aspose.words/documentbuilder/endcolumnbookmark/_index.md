---
title: "Aspose::Words::DocumentBuilder::EndColumnBookmark method"
linktitle: "EndColumnBookmark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::EndColumnBookmark 方法。将文档中的当前位置标记为列书签结束。该位置必须位于 C++ 中的表格单元格内。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


将文档中当前位置标记为列书签结束。该位置必须位于表格单元格中。

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | const System::String\& | 书签的名称。 |

### ReturnValue

刚刚创建的书签结束节点。
## 备注


列书签覆盖一系列行中的一个或多个列。要创建有效的书签，需要使用相同的 *bookmarkName* 参数调用 [StartColumnBookmark()](../) 和 [EndColumnBookmark()](../)。

格式错误的书签或名称重复的书签在保存文档时将被忽略。

插入的 [BookmarkEnd](../../bookmarkend/) 节点的实际位置可能与当前文档生成器的位置不同。

## 示例



展示如何创建列书签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// 单元格 1、2、4、5 将被标记为书签。
builder->StartColumnBookmark(u"MyBookmark_1");
// 格式错误的书签或名称重复的书签在保存文档时将被忽略。
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## 另见

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
