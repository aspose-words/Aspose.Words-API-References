---
title: "Aspose::Words::Fields::FieldAdvance::get_VerticalPosition 方法"
linktitle: "get_VerticalPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAdvance::get_VerticalPosition 方法。获取或设置字段后面的文本相对于页面顶部边缘垂直移动的点数（单位为点），在 C++ 中。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fields/fieldadvance/get_verticalposition/
---
## FieldAdvance::get_VerticalPosition method


获取或设置字段后面的文本应相对于页面顶部垂直移动的点数。

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_VerticalPosition()
```


## 示例



展示如何插入 ADVANCE 字段并编辑其属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// 以下是使用 ADVANCE 字段调整其后文本位置的两种方法。
// ADVANCE 字段的效果会持续应用，直到段落结束，
// 或另一个 ADVANCE 字段更新偏移/坐标值。
// 1 -  指定方向偏移：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  将文本移动到坐标指定的位置：
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## 另见

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
