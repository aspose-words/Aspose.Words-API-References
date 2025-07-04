---
title: Aspose::Words::Document::UpdateActualReferenceMarks method
linktitle: UpdateActualReferenceMarks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::UpdateActualReferenceMarks method. Updates the ActualReferenceMark property of all footnotes and endnotes in the document in C++.'
type: docs
weight: 95500
url: /cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Updates the [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) property of all footnotes and endnotes in the document.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
