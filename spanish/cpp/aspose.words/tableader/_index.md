---
title: "Aspose::Words::TabLeader enum"
linktitle: "TabLeader"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TabLeader enum. Especifica el tipo de línea guía mostrada bajo el carácter de tabulación en C++."
type: docs
weight: 121000
url: /es/cpp/aspose.words/tableader/
---
## TabLeader enum


Especifica el tipo de línea guía que se muestra bajo el carácter de tabulación.

```cpp
enum class TabLeader
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se muestra ninguna línea guía. |
| Puntos | 1 | La línea guía está compuesta de puntos. |
| Guiones | 2 | La línea guía está compuesta de guiones. |
| Línea | 3 | La línea guía es una sola línea. |
| Gruesa | 4 | La línea guía es una sola línea gruesa. |
| MiddleDot | 5 | La línea guía está compuesta de puntos medios. |


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
