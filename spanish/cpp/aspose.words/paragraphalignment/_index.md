---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphAlignment enum. Especifica la alineación del texto en un párrafo en C++."
type: docs
weight: 110000
url: /es/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Especifica la alineación del texto en un párrafo.

```cpp
enum class ParagraphAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Izquierda | 0 | El texto está alineado a la izquierda. |
| Centro | 1 | El texto está centrado horizontalmente. |
| Derecha | 2 | El texto está alineado a la derecha. |
| Justificar | 3 | El texto está alineado a la izquierda y a la derecha. |
| Distributed | 4 | El texto está distribuido uniformemente. |
| ArabicMediumKashida | 5 | Solo árabe. La longitud de Kashida para el texto se extiende a una longitud media determinada por el consumidor. |
| ArabicHighKashida | 7 | Solo árabe. La longitud de Kashida para el texto se extiende a su máxima longitud posible. |
| ArabicLowKashida | 8 | Solo árabe. La longitud de Kashida para el texto se extiende a una longitud ligeramente mayor. |
| ThaiDistributed | 9 | Solo tailandés. El texto está justificado con una optimización para tailandés. |
| MathElementCenterAsGroup | 10 | El único elemento [Math](../../aspose.words.math/) en una línea, alineado como 'Centered As Group'. |


## Ejemplos



Muestra cómo construir un documento Aspose.Words manualmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y termine con un nodo de documento sin hijos.
doc->RemoveAllChildren();

// Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
// Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Establezca algunas propiedades de configuración de página para la sección.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como hijo al cuerpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Finalmente, agrega contenido al documento. Crea un run,
// establece su apariencia y contenido, y luego añádelo como hijo al párrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
