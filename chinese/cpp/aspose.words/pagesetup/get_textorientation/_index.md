---
title: "Aspose::Words::PageSetup::get_TextOrientation 方法"
linktitle: "get_TextOrientation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_TextOrientation 方法。允许为整页指定 TextOrientation。默认值在 C++ 中为 Horizontal。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


允许为整页指定 [TextOrientation](./)。默认值为 [Horizontal](../../textorientation/)。

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## 示例



展示如何设置文本方向。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 将 "TextOrientation" 属性设置为 "TextOrientation.Upward"，以将所有文本旋转 90 度。
// 向右，以便所有从左到右的文本现在从上到下排列。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## 另见

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
