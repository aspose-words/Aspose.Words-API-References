---
title: Aspose::Words::MailMerging::MailMerge::get_RestartListsAtEachSection method
linktitle: get_RestartListsAtEachSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMerge::get_RestartListsAtEachSection method. Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.mailmerging/mailmerge/get_restartlistsateachsection/
---
## MailMerge::get_RestartListsAtEachSection method


Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge.

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_RestartListsAtEachSection() const
```


## Examples



Shows how to control whether or not list numbering is restarted at each section when mail merge is performed. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Section breaks with numbering.docx");

doc->get_MailMerge()->set_RestartListsAtEachSection(false);
doc->get_MailMerge()->Execute(MakeArray<String>(0), MakeArray<SharedPtr<System::Object>>(0));

doc->Save(ArtifactsDir + u"MailMerge.RestartListsAtEachSection.pdf");
```

## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
