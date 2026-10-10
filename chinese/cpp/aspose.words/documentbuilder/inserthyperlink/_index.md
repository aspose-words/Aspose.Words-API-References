---
title: "Aspose::Words::DocumentBuilder::InsertHyperlink 方法"
linktitle: "InsertHyperlink"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertHyperlink 方法。在 C++ 中向文档插入超链接。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


在文档中插入超链接。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| displayText | const System::String\& | 在文档中显示的链接文本。 |
| urlOrBookmark | const System::String\& | 链接目标。可以是 URL 或文档内部书签的名称。此方法会在 URL 的开头和结尾始终添加单引号。 |
| isBookmark | bool | **true** 表示前一个参数是文档内部书签的名称；**false** 表示前一个参数是 URL。 |

### ReturnValue

一个表示已插入字段的 [Field](../../../aspose.words.fields/field/) 对象。
## 备注


请注意，需要使用 [Font](../get_font/) 属性显式指定超链接显示文本的字体格式。

此方法内部调用 [InsertField()](../) 在文档中插入 MS Word HYPERLINK 字段。

## 示例



展示如何插入超链接字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// 插入超链接并使用自定义格式进行强调。
// 该超链接将是可点击的文本，能够将我们带到 URL 中指定的位置。
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// 在 Microsoft Word 中按 Ctrl 并左键单击文本中的链接，将通过新建的网页浏览器窗口打开该 URL。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


展示如何使用文档生成器的格式堆栈。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 设置字体格式，然后编写超链接前的文本。
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// 在堆栈上保留当前的格式配置。
builder->PushFont();

// 通过应用新样式来更改生成器的当前格式。
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// 恢复之前保存的字体格式并从堆栈中移除该元素。
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
