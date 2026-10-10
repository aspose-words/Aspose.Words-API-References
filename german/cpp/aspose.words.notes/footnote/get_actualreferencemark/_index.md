---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark method"
linktitle: "get_ActualReferenceMark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark-Methode. Gibt den tatsächlichen Text des Referenzzeichens zurück, das im Dokument für diese Fußnote in C++ angezeigt wird."
type: docs
weight: 3834
url: /de/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Liefert den tatsächlichen Text des Referenzzeichens, das im Dokument für diese Fußnote angezeigt wird.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## Beispiele



Zeigt, wie man das tatsächliche Fußnoten-Referenzzeichen erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Siehe auch

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
