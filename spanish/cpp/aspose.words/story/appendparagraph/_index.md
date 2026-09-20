---
title: "Aspose::Words::Story::AppendParagraph método"
linktitle: "AppendParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Story::AppendParagraph método. Un método abreviado que crea un objeto Paragraph con texto opcional y lo agrega al final de este objeto en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/story/appendparagraph/
---
## Story::AppendParagraph method


Un método abreviado que crea un objeto [Paragraph](../../paragraph/) con texto opcional y lo agrega al final de este objeto.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::AppendParagraph(const System::String &text)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| texto | const System::String\& | El texto del párrafo. Puede ser **null** o una cadena vacía. |

### ReturnValue

El párrafo recién creado y agregado.

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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
