---
title: Aspose::Words::Document::get_RemovePersonalInformation method
linktitle: get_RemovePersonalInformation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_RemovePersonalInformation method. Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Examples



Shows how to enable the removal of personal information during a manual save. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert some content with personal information.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// This flag is equivalent to File -> Options -> Trust Center -> Trust Center Settings... ->
// Privacy Options -> "Remove personal information from file properties on save" in Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// This option will not take effect during a save operation made using Aspose.Words.
// Personal data will be removed from our document with the flag set when we save it manually using Microsoft Word.
doc->Save(ArtifactsDir + u"Document.RemovePersonalInformation.docx");
doc = MakeObject<Document>(ArtifactsDir + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
