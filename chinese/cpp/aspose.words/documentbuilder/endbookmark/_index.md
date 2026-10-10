---
title: "Aspose::Words::DocumentBuilder::EndBookmark 方法"
linktitle: "EndBookmark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::EndBookmark 方法。 在 C++ 中将文档中的当前位置标记为书签结束。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


将文档中的当前位置标记为书签结束。

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | const System::String\& | 书签的名称。 |

### ReturnValue

刚刚创建的书签结束节点。
## 备注


文档中的书签可以重叠并跨越任意范围。要创建有效的书签，需要使用相同的 *bookmarkName* 参数调用 [StartBookmark()](../) 和 [EndBookmark()](../)。

格式错误的书签或名称重复的书签在保存文档时将被忽略。

## 示例



展示如何创建书签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 有效的书签需要在文档正文文本之间包含
// 使用匹配的书签名称创建的 BookmarkStart 和 BookmarkEnd 节点。
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


展示如何插入引用本地书签的超链接。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// 插入一个链接到书签的 HYPERLINK 域。我们可以传递字段开关
// 作为包含被引用书签名称的参数的一部分，传递给 "InsertHyperlink" 方法。
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## 另见

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
