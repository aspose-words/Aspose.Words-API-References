---
title: Aspose::Words::Notes::Footnote::get_ActualReferenceMark method
linktitle: get_ActualReferenceMark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::Footnote::get_ActualReferenceMark method. Gets the actual text of the reference mark displayed in the document for this footnote in C++.'
type: docs
weight: 3834
url: /cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Gets the actual text of the reference mark displayed in the document for this footnote.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## Examples



Shows how to get actual footnote reference mark. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## See Also

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
