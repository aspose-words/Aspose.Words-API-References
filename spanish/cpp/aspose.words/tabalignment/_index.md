---
title: "Aspose::Words::TabAlignment enum"
linktitle: "TabAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TabAlignment enum. Especifica la alineación/tipo de una tabulación en C++."
type: docs
weight: 120000
url: /es/cpp/aspose.words/tabalignment/
---
## TabAlignment enum


Especifica la alineación/tipo de una tabulación.

```cpp
enum class TabAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Izquierda | 0 | Alinea a la izquierda el texto después de la tabulación. |
| Centro | 1 | Centra el texto alrededor de la tabulación. |
| Derecha | 2 | Alinea a la derecha el texto en la tabulación. |
| Decimal | 3 | Alinea el texto en el punto decimal. |
| Bar | 4 | Dibuja una barra vertical en la posición de la tabulación. |
| List | 6 | La tabulación es un delimitador entre el número/viñeta y el texto en un elemento de lista. |
| Clear | 7 | Elimina cualquier tabulación en esta posición. |


## Ejemplos



Muestra cómo establecer tabulaciones personalizadas para un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Si estamos en un párrafo sin tabulaciones en esta colección,
// el cursor avanzará 36 puntos cada vez que presionemos la tecla Tab en Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Podemos agregar tabulaciones personalizadas en Microsoft Word si habilitamos la regla a través de la pestaña "View".
// Cada unidad en esta regla equivale a dos tabulaciones predeterminadas, lo que son 72 puntos.
// Podemos agregar tabulaciones personalizadas programáticamente así.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Podemos ver estas tabulaciones en Microsoft Word habilitando la regla a través de "View" -> "Show" -> "Ruler".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Cualquier carácter de tabulación que agreguemos utilizará las tabulaciones en la regla y puede,
// dependiendo del valor del líder de tabulación, dejar una línea entre los destinos de salida y llegada de la tabulación.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
