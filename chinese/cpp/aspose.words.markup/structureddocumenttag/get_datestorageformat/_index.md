---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat method"
linktitle: "get_DateStorageFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat method. 获取/设置当 SDT 绑定到文档数据存储的 XML 节点时，日期 SDT 的日期存储格式。默认值为 C++ 中的 DateTime。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/get_datestorageformat/
---
## StructuredDocumentTag::get_DateStorageFormat method


获取/设置当 **SDT** 绑定到文档数据存储的 XML 节点时，日期 SDT 的日期存储格式。默认值为 [DateTime](../../sdtdatestorageformat/)。

```cpp
Aspose::Words::Markup::SdtDateStorageFormat Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat()
```

## 备注


访问此属性仅适用于 [Date](../../sdttype/) SDT 类型。

对于所有其他 SDT 类型，将会出现异常。

## 示例



展示如何使用结构化文档标签提示用户输入日期。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入一个提示用户输入日期的结构化文档标签。
// 在 Microsoft Word 中，此元素称为 "Date picker content control"。
// 当我们在 Microsoft Word 中点击此标签右端的箭头时，
// 我们会看到一个可点击的日历形式的弹出窗口。
// 我们可以使用该弹出窗口选择标签将显示的日期。
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// 根据沙特阿拉伯阿拉伯语地区设置显示日期。
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// 设置显示日期的格式。
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// 根据伊斯兰历显示日期。
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// 在用户在 Microsoft Word 中选择日期之前，标签将显示文本 "Click here to enter a date."。
// 根据标签的日历，设置 "FullDate" 属性以使标签显示默认日期。
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## 另见

* Enum [SdtDateStorageFormat](../../sdtdatestorageformat/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
