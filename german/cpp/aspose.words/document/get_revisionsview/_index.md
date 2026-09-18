---
title: "Aspose::Words::Document::get_RevisionsView Methode"
linktitle: "get_RevisionsView"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_RevisionsView-Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob mit der Original- oder der überarbeiteten Version eines Dokuments in C++ gearbeitet werden soll."
type: docs
weight: 47000
url: /de/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


Liest oder legt einen Wert fest, der angibt, ob mit der Original- oder der überarbeiteten Version eines Dokuments gearbeitet werden soll.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


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

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
