---
title: Aspose::Words::Notes::Footnote::get_ActualReferenceMark method
linktitle: get_ActualReferenceMark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::Footnote::get_ActualReferenceMark method. Gets the actual text of the reference mark displayed in the document for this footnote in C++.'
type: docs
weight: 10250
url: /cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Gets the actual text of the reference mark displayed in the document for this footnote.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```

## Remarks

 To initially populate values of this property for all reference marks of the document, or to update the values after changes in the document that might affect the reference marks, you must execute the [UpdateActualReferenceMarks](../../../aspose.words/document/updateactualreferencemarks/) method. Updating fields ([UpdateFields](../../../aspose.words/document/updatefields/)) may also be necessary to get the correct result. 
## Examples


Shows how to get actual footnote reference mark.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Footnotes and endnotes.docx"));

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```
## See Also

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
