---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::RevisionsView enum. Permite especificar si trabajar con la versión original o revisada de un documento en C++."
type: docs
weight: 112000
url: /es/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Permite especificar si se trabaja con la versión original o revisada de un documento.

```cpp
enum class RevisionsView
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Original | 0 | Especifica la versión original de un documento. |
| Final | 1 | Especifica la versión revisada de un documento. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
