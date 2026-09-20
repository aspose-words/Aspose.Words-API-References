---
title: "Aspose::Words::HeaderFooter::get_IsLinkedToPrevious método"
linktitle: "get_IsLinkedToPrevious"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::HeaderFooter::get_IsLinkedToPrevious método. Verdadero si este encabezado o pie de página está vinculado al encabezado o pie de página correspondiente en la sección anterior en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/headerfooter/get_islinkedtoprevious/
---
## HeaderFooter::get_IsLinkedToPrevious method


Verdadero si este encabezado o pie de página está vinculado al encabezado o pie de página correspondiente en la sección anterior.

```cpp
bool Aspose::Words::HeaderFooter::get_IsLinkedToPrevious()
```

## Observaciones


El valor predeterminado es **true**.

Nota, cuando vinculas un encabezado o pie de página, su contenido se borra.

## Ejemplos



Muestra cómo enlazar encabezados y pies de página entre secciones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Mueva a la primera sección y cree un encabezado y un pie de página. Por defecto,
// el encabezado y el pie de página solo aparecerán en las páginas de la sección que los contiene.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Podemos enlazar los encabezados/pies de página de una sección a los encabezados/pies de página de la sección anterior
// para permitir que la sección que enlaza muestre los encabezados/pies de página de la sección enlazada.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Cada sección seguirá teniendo sus propios objetos de encabezado/pie de página. Cuando enlazamos secciones,
// la sección que enlaza mostrará los encabezados/pies de página de la sección enlazada mientras conserva los suyos propios.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Enlace los encabezados/pies de página de la tercera sección a los encabezados/pies de página de la segunda sección.
// La segunda sección ya enlaza a los encabezados/pies de página de la primera sección,
// por lo que enlazar a la segunda sección creará una cadena de enlaces.
// Las secciones primera, segunda y ahora la tercera mostrarán todos los encabezados de la primera sección.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Podemos desenlazar los encabezados/pies de página de una sección anterior pasando "false" al llamar al método LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// También podemos seleccionar solo un tipo específico de encabezado/pie de página para enlazar usando este método.
// La tercera sección ahora tendrá el mismo pie de página que las secciones segunda y primera, pero no el encabezado.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Los encabezados/pies de página de la primera sección no pueden enlazarse a nada porque no hay una sección anterior.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Todos los encabezados/pies de página de la segunda sección están enlazados a los encabezados/pies de página de la primera sección.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// En la tercera sección, solo el pie de página está vinculado al pie de página de la primera sección a través de la segunda sección.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Ver también

* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
