---
title: "Aspose::Words::Fields::FieldGoToButton::get_Location 方法"
linktitle: "get_Location"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldGoToButton::get_Location 方法。获取或设置书签的名称、页码或其他跳转项（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


获取或设置书签、页码或其他跳转目标的名称。

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## 示例



展示如何插入 GOTOBUTTON 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加一个 GOTOBUTTON 字段。当我们在 Microsoft Word 中双击此字段时，
// 它会将文本光标移动到 Location 属性引用的书签名称所在的位置。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// 插入一个有效的书签供该字段引用。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## 另见

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
