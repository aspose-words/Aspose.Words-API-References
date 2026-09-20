---
title: "Aspose::Words::HeaderFooterCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::HeaderFooterCollection::idx_get método. Recupera un HeaderFooter del tipo especificado en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/headerfootercollection/idx_get/
---
## HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType) method


Recupera un [HeaderFooter](../../headerfooter/) del tipo especificado.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Un valor de [HeaderFooterType](../../headerfootertype/) que especifica el tipo de encabezado/pie de página a recuperar. |

## Ejemplos



Muestra cómo eliminar todos los pies de página de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Itera a través de cada sección y elimina los pies de página de todo tipo.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Hay tres tipos de pies de página y encabezados.
    // 1 -  El encabezado/pie de página "First", que solo aparece en la primera página de una sección.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  El encabezado/pie de página "Primary", que aparece en las páginas impares.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  El encabezado/pie de página "Even", que aparece en las páginas pares.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Muestra cómo reemplazar texto en el pie de página de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Ver también

* Class [HeaderFooter](../../headerfooter/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::idx_get(int32_t) method


Recupera un [HeaderFooter](../../headerfooter/) en el índice dado.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la colección. |
## Observaciones


El índice comienza en cero.

Se permiten índices negativos e indican acceso desde el final de la colección. Por ejemplo, -1 significa el último elemento, -2 el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos en la lista, esto devuelve una referencia nula.

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

* Class [HeaderFooter](../../headerfooter/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
