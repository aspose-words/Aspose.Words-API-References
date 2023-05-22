---
title: Aspose::Words::Fields::FieldInclude::get_TextConverter method
linktitle: get_TextConverter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldInclude::get_TextConverter method. Gets or sets the name of the text converter for the format of the included file in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldinclude/get_textconverter/
---
## FieldInclude::get_TextConverter method


Gets or sets the name of the text converter for the format of the included file.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_TextConverter() override
```


## Examples



Shows how to create an INCLUDE field, and set its properties. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// We can use an INCLUDE field to import a portion of another document in the local file system.
// The bookmark from the other document that we reference with this field contains this imported portion.
auto field = System::ExplicitCast<FieldInclude>(builder->InsertField(FieldType::FieldInclude, true));
field->set_SourceFullName(MyDir + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.INCLUDE.docx");
```

## See Also

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
