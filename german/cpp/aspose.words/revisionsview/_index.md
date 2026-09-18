---
title: "Aspose::Words::RevisionsView‑Enum"
linktitle: "RevisionsView"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionsView‑Enum. Ermöglicht die Angabe, ob mit der Original‑ oder der überarbeiteten Version eines Dokuments in C++ gearbeitet werden soll."
type: docs
weight: 112000
url: /de/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Ermöglicht die Angabe, ob mit der Original- oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

```cpp
enum class RevisionsView
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Original | 0 | Gibt die Originalversion eines Dokuments an. |
| Final | 1 | Gibt die überarbeitete Version eines Dokuments an. |


## Beispiele



Zeigt, wie man zwischen der überarbeiteten und der Originalansicht eines Dokuments wechselt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Zeigt das Dokumentobjekt, als wären alle Änderungen akzeptiert. Unterstützt derzeit Listenelemente.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
