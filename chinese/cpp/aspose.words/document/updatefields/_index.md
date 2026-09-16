---
title: "Aspose::Words::Document::UpdateFields 方法"
linktitle: "UpdateFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UpdateFields 方法。更新整个文档中字段的值（C++）。"
type: docs
weight: 96000
url: /zh/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


更新整个文档中字段的值。

```cpp
void Aspose::Words::Document::UpdateFields()
```

## 备注


当您打开、修改然后保存文档时，Aspose.Words 不会自动更新字段，它会保持原样。因此，如果您以编程方式修改了文档并希望确保保存的文档中出现正确（已计算）的字段值，通常需要在保存之前调用此方法。

执行邮件合并后无需更新字段，因为邮件合并本身是一种字段更新，会自动更新文档中的所有字段。

此方法并未更新所有字段类型。有关受支持字段类型的详细列表，请参阅程序员指南。

此方法不更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。当您渲染文档或调用 [UpdatePageLayout](../updatepagelayout/) 时，页面布局相关的字段会被更新。

如果文档更改影响了字段类型，请在更新字段之前使用 [NormalizeFieldTypes](../normalizefieldtypes/) 方法。

要在文档的特定部分更新字段，请使用 [UpdateFields](../../range/updatefields/)。

## 示例



展示如何使用标题样式作为条目，将目录（TOC）插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在文档的首页插入目录。
// 配置目录以捕获标题级别 1 到 3 的段落。
// 此外，将其条目设置为超链接，以便我们
// 在 Microsoft Word 中左击时跳转到标题所在位置。
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 通过添加带有标题样式的段落来填充目录。
// 每个级别在 1 到 3 之间的标题都会在目录中创建一个条目。
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// 目录是需要更新以显示最新结果的字段类型。
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


展示如何使用 QUOTE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入 QUOTE 字段，它将显示其 Text 属性的值。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// 插入 QUOTE 字段并在其内部嵌套 DATE 字段。
// DATE 字段在每次使用 Microsoft Word 打开文档时都会将其值更新为当前日期。
// 像这样将 DATE 字段嵌套在 QUOTE 字段中会冻结其值
// 至我们创建文档的日期。
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// 更新所有字段以显示其正确结果。
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


展示如何设置用户详细信息，并使用字段显示它们。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 UserInformation 对象，并将其设置为显示用户信息的字段的数据源。
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，这些字段显示
// 我们上面创建的 UserInformation 对象的相应属性。
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// 字段选项对象还具有一个静态默认用户，所有文档中的字段都可以引用它。
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
