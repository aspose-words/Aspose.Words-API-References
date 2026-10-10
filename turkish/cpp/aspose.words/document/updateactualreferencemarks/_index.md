---
title: "Aspose::Words::Document::UpdateActualReferenceMarks metodu"
linktitle: "UpdateActualReferenceMarks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UpdateActualReferenceMarks metodu. Belgedeki tüm dipnot ve sonnotların ActualReferenceMark özelliğini C++'ta günceller."
type: docs
weight: 95500
url: /tr/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Belgedeki tüm dipnot ve sonnotların [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) özelliğini günceller.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
```


## Örnekler



Gerçek dipnot referans işaretinin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
