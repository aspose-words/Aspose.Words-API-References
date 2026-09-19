---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionsView enum. Consente di specificare se lavorare con la versione originale o revisionata di un documento in C++."
type: docs
weight: 112000
url: /it/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Consente di specificare se lavorare con la versione originale o revisionata di un documento.

```cpp
enum class RevisionsView
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Originale | 0 | Specifica la versione originale di un documento. |
| Finale | 1 | Specifica la versione revisionata di un documento. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
