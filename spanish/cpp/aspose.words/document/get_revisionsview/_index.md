---
title: "Aspose::Words::Document::get_RevisionsView método"
linktitle: "get_RevisionsView"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_RevisionsView método. Obtiene o establece un valor que indica si se trabaja con la versión original o revisada de un documento en C++."
type: docs
weight: 47000
url: /es/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


Obtiene o establece un valor que indica si trabajar con la versión original o revisada de un documento.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


## Ejemplos



Muestra cómo cambiar entre la vista revisada y la original de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Visualiza el objeto documento como si todas las revisiones estuvieran aceptadas. Actualmente soporta etiquetas de lista.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Ver también

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
