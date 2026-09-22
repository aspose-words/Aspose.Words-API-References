---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark metodu"
linktitle: "get_ActualReferenceMark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark metodu. Bu dipnot için belgede gösterilen referans işaretinin gerçek metnini C++'ta alır."
type: docs
weight: 3834
url: /tr/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Bu dipnot için belgede gösterilen referans işaretinin gerçek metnini alır.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
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

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
