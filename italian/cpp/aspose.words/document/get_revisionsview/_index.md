---
title: "Metodo Aspose::Words::Document::get_RevisionsView"
linktitle: "get_RevisionsView"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_RevisionsView. Ottiene o imposta un valore che indica se lavorare con la versione originale o revisionata di un documento in C++."
type: docs
weight: 47000
url: /it/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


Ottiene o imposta un valore che indica se lavorare con la versione originale o revisionata di un documento.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


## Esempi



Mostra come passare dalla visualizzazione revisionata a quella originale di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Visualizza l'oggetto documento come se tutte le revisioni fossero accettate. Attualmente supporta le etichette di elenco.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Vedi anche

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
