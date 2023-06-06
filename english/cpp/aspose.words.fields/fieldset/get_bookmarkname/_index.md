---
title: Aspose::Words::Fields::FieldSet::get_BookmarkName method
linktitle: get_BookmarkName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldSet::get_BookmarkName method. Gets or sets the name of the bookmark in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldset/get_bookmarkname/
---
## FieldSet::get_BookmarkName method


Gets or sets the name of the bookmark.

```cpp
System::String Aspose::Words::Fields::FieldSet::get_BookmarkName()
```


## Examples



Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Name bookmarked text with a SET field.
// This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
auto fieldSet = System::ExplicitCast<FieldSet>(builder->InsertField(FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refer to the bookmark by name in a REF field and display its contents.
auto fieldRef = System::ExplicitCast<FieldRef>(builder->InsertField(FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(ArtifactsDir + u"Field.SET.REF.docx");
```

## See Also

* Class [FieldSet](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
