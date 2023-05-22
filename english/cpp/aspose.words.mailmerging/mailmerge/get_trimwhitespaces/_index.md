---
title: Aspose::Words::MailMerging::MailMerge::get_TrimWhitespaces method
linktitle: get_TrimWhitespaces
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMerge::get_TrimWhitespaces method. Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.mailmerging/mailmerge/get_trimwhitespaces/
---
## MailMerge::get_TrimWhitespaces method


Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_TrimWhitespaces() const
```


## Examples



Shows how to trim whitespaces from values of a data source while executing a mail merge. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertField(u"MERGEFIELD myMergeField", nullptr);

doc->get_MailMerge()->set_TrimWhitespaces(trimWhitespaces);
doc->get_MailMerge()->Execute(MakeArray<String>({u"myMergeField"}),
                              MakeArray<SharedPtr<System::Object>>({System::ObjectExt::Box<String>(u"\t hello world! ")}));

ASSERT_EQ(trimWhitespaces ? String(u"hello world!\f") : String(u"\t hello world! \f"), doc->GetText());
```

## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
