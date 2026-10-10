---
title: "Aspose::Words::Document::get_ShadeFormData 方法"
linktitle: "get_ShadeFormData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_ShadeFormData 方法。指定是否在 C++ 中打开表单字段的灰色阴影。"
type: docs
weight: 49000
url: /zh/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


指定是否在表单字段上启用灰色阴影。

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## 示例



展示如何对表单字段应用灰色阴影。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// 我们可以关闭灰色阴影，使书签文本与其他文本融合。
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
