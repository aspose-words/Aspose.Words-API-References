---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat 方法"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat 方法。获取或设置指示在 C++ 中是否使用不变文化解析数字格式的值。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


获取或设置指示是否使用不变区域性解析数字格式的值。

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## 备注


当此属性设置为 **true** 时，数字格式取自不变文化。

当此属性设置为 **false** 时，数字格式取自当前线程的文化。

默认值为 **false**。

## 示例



展示如何根据不变文化格式化数字。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// 有时，在某些文化环境下，字段可能无法正确格式化其数字。
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// 为了解决此问题，我们可以更改整个线程的文化。
// 另一种解决方法是设置此标志，
// 它使所有字段在格式化数字时使用不变文化。
// 这种方式使我们能够避免为整个线程更改文化。
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## 另见

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
