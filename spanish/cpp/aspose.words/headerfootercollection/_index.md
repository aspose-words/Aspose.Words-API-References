---
title: "Aspose::Words::HeaderFooterCollection clase"
linktitle: "HeaderFooterCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::HeaderFooterCollection clase. Proporciona acceso tipado a los nodos HeaderFooter de una Section. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


Proporciona acceso tipado a los nodos [HeaderFooter](../headerfooter/) de una [Section](../section/). Para obtener más información, visite el artículo de documentación [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/).

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega un nodo al final de la colección. |
| [Clear](../nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina si un nodo está en la colección. |
| [get_Count](../nodecollection/get_count/)() | Obtiene el número de nodos en la colección. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un [HeaderFooter](../headerfooter/) en el índice dado. |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | Recupera un [HeaderFooter](../headerfooter/) del tipo especificado. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | Enlaza o desenlaza todos los encabezados y pies de página con los encabezados y pies de página correspondientes en la sección anterior. |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | Enlaza o desenlaza el encabezado o pie de página especificado con el encabezado o pie de página correspondiente en la sección anterior. |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todos los **HeaderFooter**s de la colección a una nueva matriz de **HeaderFooter**s. |
| static [Type](./type/)() |  |
## Observaciones


Puede haber como máximo un [HeaderFooter](../headerfooter/)

de cada [HeaderFooterType](../headerfootertype/) por [Section](../section/).

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

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

## Ver también

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
