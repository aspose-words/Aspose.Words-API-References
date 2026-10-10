---
title: "Aspose::Words::Fields::FieldHyperlink::get_SubAddress 方法"
linktitle: "get_SubAddress"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldHyperlink::get_SubAddress 方法。获取或设置文件中的位置（例如书签），此超链接将在 C++ 中跳转到该位置。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.fields/fieldhyperlink/get_subaddress/
---
## FieldHyperlink::get_SubAddress method


获取或设置文件中的位置，例如书签，此超链接将跳转到该位置。

```cpp
System::String Aspose::Words::Fields::FieldHyperlink::get_SubAddress()
```


## 示例



展示如何使用 HYPERLINK 字段链接本地文件系统中的文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，然后将光标定位到指定的书签。
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，并自动滚动到指定的 iframe。
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## 另见

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
