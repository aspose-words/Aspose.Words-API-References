---
title: "Aspose::Words::TabStopCollection clase"
linktitle: "TabStopCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TabStopCollection clase. Una colección de objetos TabStop que representan tabulaciones personalizadas para un párrafo o un estilo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 69000
url: /es/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


Una colección de objetos [TabStop](../tabstop/) que representan tabulaciones personalizadas para un párrafo o un estilo. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Agrega o reemplaza una tabulación en la colección. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Agrega o reemplaza una tabulación en la colección. |
| [After](./after/)(double) | Obtiene la primera tabulación a la derecha de la posición especificada. |
| [Before](./before/)(double) | Obtiene la primera tabulación a la izquierda de la posición especificada. |
| [Clear](./clear/)() | Elimina todas las posiciones de tabulación. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Determina si la [TabStopCollection](./) especificada es igual en valor a la [TabStopCollection](./) actual. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_Count](./get_count/)() | Obtiene el número de tabulaciones en la colección. |
| [GetHashCode](./gethashcode/)() const override | Sirve como función hash para este tipo. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Obtiene el índice de una tabulación con la posición especificada en puntos. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Obtiene la posición (en puntos) de la tabulación en el índice especificado. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene una tabulación en el índice dado. |
| [idx_get](./idx_get/)(double) | Obtiene una tabulación en la posición especificada. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Elimina una tabulación en el índice especificado de la colección. |
| [RemoveByPosition](./removebyposition/)(double) | Elimina una tabulación en la posición especificada de la colección. |
| static [Type](./type/)() |  |
## Observaciones


En los documentos de Microsoft Word, una tabulación puede definirse en las propiedades de un estilo de párrafo o directamente en las propiedades de un párrafo. Un estilo puede basarse en otro estilo. Por lo tanto, el conjunto completo de tabulaciones para un objeto dado es una combinación de tabulaciones definidas directamente en este objeto y tabulaciones heredadas de los estilos padre.

En Aspose.Words, cuando se obtiene una [TabStopCollection](./) para un párrafo o un estilo, contiene solo las tabulaciones personalizadas definidas directamente para ese párrafo o estilo. La colección no incluye tabulaciones definidas en los estilos padre ni las tabulaciones predeterminadas.

## Ejemplos



Muestra cómo trabajar con la colección de tabulaciones de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 puntos equivalen a una "pulgada" en la regla de tabulaciones de Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Cada carácter "tab" lleva el cursor del constructor a la ubicación de la siguiente tabulación.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Cada párrafo obtiene su colección de tabulaciones, que clona sus valores de la colección de tabulaciones del constructor de documentos.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Una colección de tabulaciones puede indicarnos TabStops antes y después de ciertas posiciones.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Podemos borrar la colección de tabulaciones de un párrafo para volver al comportamiento de tabulación predeterminado.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Ver también

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
