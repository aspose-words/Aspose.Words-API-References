---
title: AcceptAllRevisions
second_title: Aspose.Words for C++ API Reference
description: Accepts all tracked changes in the document.
type: docs
weight: 27
url: /cpp/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method


Accepts all tracked changes in the document.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Examples




Shows how to accept all tracking changes in the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Edit the document while tracking changes to create a few revisions.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// We can iterate through every revision and accept/reject it as a part of our document.
// If we know we wish to accept every revision, we can do it more straightforwardly so by calling this method.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

