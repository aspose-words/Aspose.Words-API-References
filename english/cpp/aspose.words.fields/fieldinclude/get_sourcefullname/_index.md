---
title: get_SourceFullName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the location of the document.
type: docs
weight: 27
url: /cpp/aspose.words.fields/fieldinclude/get_sourcefullname/
---
## FieldInclude::get_SourceFullName method


Gets or sets the location of the document.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_SourceFullName() override
```


## Examples



Shows how to create an INCLUDE field, and set its properties. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// We can use an INCLUDE field to import a portion of another document in the local file system.
// The bookmark from the other document that we reference with this field contains this imported portion.
auto field = System::DynamicCast<FieldInclude>(builder->InsertField(FieldType::FieldInclude, true));
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
* Library [Aspose.Words](../../../)
