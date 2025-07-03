---
title: Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically method
linktitle: get_ResizeVertically
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically method. Gets or sets whether to resize the picture vertically from the source in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldincludepicture/get_resizevertically/
---
## FieldIncludePicture::get_ResizeVertically method


Gets or sets whether to resize the picture vertically from the source.

```cpp
bool Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically()
```


## Examples



Shows how to insert images using IMPORT and INCLUDEPICTURE fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two similar field types that we can use to display images linked from the local file system.
// 1 -  The INCLUDEPICTURE field:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Apply the PNG32.FLT filter.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  The IMPORT field:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## See Also

* Class [FieldIncludePicture](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
