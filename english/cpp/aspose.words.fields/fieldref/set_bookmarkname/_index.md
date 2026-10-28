---
title: Aspose::Words::Fields::FieldRef::set_BookmarkName method
linktitle: set_BookmarkName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldRef::set_BookmarkName method. Sets the referenced bookmark''s name in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.fields/fieldref/set_bookmarkname/
---
## FieldRef::set_BookmarkName method


Sets the referenced bookmark's name.

```cpp
void Aspose::Words::Fields::FieldRef::set_BookmarkName(const System::String & value)
```

## Examples


Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Name bookmarked text with a SET field.
// This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refer to the bookmark by name in a REF field and display its contents.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```
## See Also

* Class [FieldRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
