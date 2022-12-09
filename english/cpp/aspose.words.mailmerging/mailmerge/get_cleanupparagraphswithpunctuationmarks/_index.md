---
title: get_CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the RemoveEmptyParagraphs option is specified.
type: docs
weight: 66
url: /cpp/aspose.words.mailmerging/mailmerge/get_cleanupparagraphswithpunctuationmarks/
---
## MailMerge::get_CleanupParagraphsWithPunctuationMarks method


Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [RemoveEmptyParagraphs](../../mailmergecleanupoptions/) option is specified.

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks() const
```

## Remarks


The default value is **true**. Here is the complete list of cleanable punctuation marks:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿



## Examples



Shows how to remove paragraphs with punctuation marks after a mail merge operation. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto mergeFieldOption1 = System::DynamicCast<FieldMergeField>(builder->InsertField(u"MERGEFIELD", u"Option_1"));
mergeFieldOption1->set_FieldName(u"Option_1");

builder->Write(punctuationMark);

auto mergeFieldOption2 = System::DynamicCast<FieldMergeField>(builder->InsertField(u"MERGEFIELD", u"Option_2"));
mergeFieldOption2->set_FieldName(u"Option_2");

// Configure the "CleanupOptions" property to remove any empty paragraphs that this mail merge would create.
doc->get_MailMerge()->set_CleanupOptions(MailMergeCleanupOptions::RemoveEmptyParagraphs);

// Setting the "CleanupParagraphsWithPunctuationMarks" property to "true" will also count paragraphs
// with punctuation marks as empty and will get the mail merge operation to remove them as well.
// Setting the "CleanupParagraphsWithPunctuationMarks" property to "false"
// will remove empty paragraphs, but not ones with punctuation marks.
// This is a list of punctuation marks that this property concerns: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc->get_MailMerge()->set_CleanupParagraphsWithPunctuationMarks(cleanupParagraphsWithPunctuationMarks);

doc->get_MailMerge()->Execute(MakeArray<String>({u"Option_1", u"Option_2"}), MakeArray<SharedPtr<System::Object>>({nullptr, nullptr}));

doc->Save(ArtifactsDir + u"MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words](../../../)
