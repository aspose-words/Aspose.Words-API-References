---
title: "Aspose::Words::Paragraph::get_IsEndOfHeaderFooter método"
linktitle: "get_IsEndOfHeaderFooter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Paragraph::get_IsEndOfHeaderFooter método. Verdadero si este párrafo es el último párrafo en el HeaderFooter (historia de texto principal) de una Section; falso en caso contrario en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/paragraph/get_isendofheaderfooter/
---
## Paragraph::get_IsEndOfHeaderFooter method


Verdadero si este párrafo es el último párrafo en el [HeaderFooter](../../headerfooter/) (historia de texto principal) de una [Section](../../section/); falso en caso contrario.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfHeaderFooter()
```


## Ejemplos



Muestra cómo crear un encabezado y un pie de página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un encabezado y agrega un párrafo a él. El texto en ese párrafo
// aparecerá en la parte superior de cada página de esta sección, sobre el texto principal del cuerpo.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Crea un pie de página y agrega un párrafo a él. El texto en ese párrafo
// aparecerá en la parte inferior de cada página de esta sección, bajo el texto principal del cuerpo.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## Ver también

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
