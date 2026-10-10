---
title: "Aspose::Words::Fields::FieldStyleRef::get_SuppressNonDelimiters 方法"
linktitle: "get_SuppressNonDelimiters"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldStyleRef::get_SuppressNonDelimiters 方法。获取或设置是否在 C++ 中抑制非分隔符字符。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fields/fieldstyleref/get_suppressnondelimiters/
---
## FieldStyleRef::get_SuppressNonDelimiters method


获取或设置是否抑制非分隔符字符。

```cpp
bool Aspose::Words::Fields::FieldStyleRef::get_SuppressNonDelimiters()
```


## 示例



展示如何使用 STYLEREF 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 Microsoft Word 列表模板创建基于列表。
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// 此生成的列表将显示 "1.a )"。
// 括号前的空格是非分隔符字符，我们可以抑制它。
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"\x0000" u".");
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"\x0001" u" )");

// 添加文本并应用段落样式，STYLEREF 字段将引用这些样式。
builder->get_ListFormat()->set_List(list);
builder->get_ListFormat()->ListIndent();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(u"Item 2");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 3");
builder->get_ListFormat()->RemoveNumbers();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// 在页眉中放置 STYLEREF 字段，并显示文档中第一个 "List Paragraph" 样式的文本。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// 在页脚中放置 STYLEREF 字段，并让它显示最后的文本。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// 我们还可以使用 STYLEREF 字段引用列表的编号。
builder->Write(u"\nParagraph number: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumber(true);

builder->Write(u"\nParagraph number, relative context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInRelativeContext(true);

builder->Write(u"\nParagraph number, full context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);

builder->Write(u"\nParagraph number, full context, non-delimiter chars suppressed: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);
field->set_SuppressNonDelimiters(true);

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.STYLEREF.docx");
```

## 另见

* Class [FieldStyleRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
