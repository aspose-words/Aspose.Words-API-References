---
title: "Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically 方法"
linktitle: "get_ResizeVertically"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically 方法。获取或设置在 C++ 中是否从源垂直调整图片大小。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fields/fieldincludepicture/get_resizevertically/
---
## FieldIncludePicture::get_ResizeVertically method


获取或设置是否垂直调整来源图片的大小。

```cpp
bool Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically()
```


## 示例



展示如何使用 IMPORT 和 INCLUDEPICTURE 字段插入图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是两种相似的字段类型，可用于显示来自本地文件系统的链接图像。
// 1 -  INCLUDEPICTURE 字段：
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// 应用 PNG32.FLT 过滤器。
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  IMPORT 字段：
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## 另见

* Class [FieldIncludePicture](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
