---
title: Aspose::Words::Fields::FieldSet::get_BookmarkText method
linktitle: get_BookmarkText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldSet::get_BookmarkText method. Gets or sets the new text of the bookmark in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fieldset/get_bookmarktext/
---
## FieldSet::get_BookmarkText method


Gets or sets the new text of the bookmark.

```cpp
System::String Aspose::Words::Fields::FieldSet::get_BookmarkText()
```


## Examples



Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Name bookmarked text with a SET field.
// This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refer to the bookmark by name in a REF field and display its contents.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## See Also

* Class [FieldSet](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
