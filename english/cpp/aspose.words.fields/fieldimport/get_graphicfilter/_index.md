---
title: Aspose::Words::Fields::FieldImport::get_GraphicFilter method
linktitle: get_GraphicFilter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldImport::get_GraphicFilter method. Gets or sets the name of the filter for the format of the graphic that is to be inserted in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldimport/get_graphicfilter/
---
## FieldImport::get_GraphicFilter method


Gets or sets the name of the filter for the format of the graphic that is to be inserted.

```cpp
System::String Aspose::Words::Fields::FieldImport::get_GraphicFilter()
```


## Examples



Shows how to insert images using IMPORT and INCLUDEPICTURE fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two similar field types that we can use to display images linked from the local file system.
// 1 -  The INCLUDEPICTURE field:
auto fieldIncludePicture = System::ExplicitCast<FieldIncludePicture>(builder->InsertField(FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(ImageDir + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Apply the PNG32.FLT filter.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  The IMPORT field:
auto fieldImport = System::ExplicitCast<FieldImport>(builder->InsertField(FieldType::FieldImport, true));
fieldImport->set_SourceFullName(ImageDir + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## See Also

* Class [FieldImport](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
