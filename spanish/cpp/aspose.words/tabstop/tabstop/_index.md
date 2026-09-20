---
title: "Constructor TabStop de Aspose::Words::TabStop"
linktitle: "TabStop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor TabStop de Aspose::Words::TabStop. Inicializa una nueva instancia de esta clase en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/tabstop/tabstop/
---
## TabStop::TabStop(double) constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::TabStop::TabStop(double position)
```


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

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStop::TabStop(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::TabStop::TabStop(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double | La posición de la tabulación en puntos. |
| alignment | Aspose::Words::TabAlignment | Un valor [TabAlignment](../../tabalignment/) que especifica la alineación del texto en esta tabulación. |
| leader | Aspose::Words::TabLeader | Un valor [TabLeader](../../tableader/) que especifica el tipo de línea guía mostrada bajo el carácter de tabulación. |

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

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
