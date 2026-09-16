---
title: "Aspose::Words::Fields::FieldQuote::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldQuote::get_Text 方法。获取或设置要检索的文本（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


获取或设置要检索的文本。

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## 示例



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

## 另见

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
