---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark metod"
linktitle: "get_ActualReferenceMark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark metod. Hämtar den faktiska texten för referensmarkeringen som visas i dokumentet för denna fotnot i C++."
type: docs
weight: 3834
url: /sv/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Hämtar den faktiska texten för referensmärket som visas i dokumentet för denna fotnot.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## Exempel



Visar hur man hämtar den faktiska fotnotreferensmarkeringen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Se även

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
