---
title: Aspose::Words::Fields::FieldInclude::set_TextConverter method
linktitle: set_TextConverter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldInclude::set_TextConverter method. Sets the name of the text converter for the format of the included file in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.fields/fieldinclude/set_textconverter/
---
## FieldInclude::set_TextConverter method


Sets the name of the text converter for the format of the included file.

```cpp
void Aspose::Words::Fields::FieldInclude::set_TextConverter(const System::String & value)
```

## Examples


Shows how to create an INCLUDE field, and set its properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// We can use an INCLUDE field to import a portion of another document in the local file system.
// The bookmark from the other document that we reference with this field contains this imported portion.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```
## See Also

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
