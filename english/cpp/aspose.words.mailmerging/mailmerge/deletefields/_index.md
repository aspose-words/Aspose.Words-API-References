---
title: DeleteFields
second_title: Aspose.Words for C++ API Reference
description: Removes mail merge related fields from the document.
type: docs
weight: 1
url: /cpp/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method


Removes mail merge related fields from the document.

```cpp
void Aspose::Words::MailMerging::MailMerge::DeleteFields()
```


This method removes MERGEFIELD and NEXT fields from the document.

This method could be useful if your mail merge operation does not always need to populate all fields in the document. Use this method to remove all remaining mail merge fields.

## Examples




Shows how to delete all MERGEFIELDs from a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Dear ");
builder->InsertField(u" MERGEFIELD FirstName ");
builder->Write(u" ");
builder->InsertField(u" MERGEFIELD LastName ");
builder->Writeln(u",");
builder->Writeln(u"Greetings!");

ASSERT_EQ(u"Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!",
          doc->GetText().Trim());

doc->get_MailMerge()->DeleteFields();

ASSERT_EQ(u"Dear  ,\rGreetings!", doc->GetText().Trim());
```

