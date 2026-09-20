---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl método"
linktitle: "get_FarEastLineBreakControl"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl método. Obtiene o establece una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Obtiene o establece una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
```


## Ejemplos



Muestra cómo establecer propiedades especiales para la tipografía asiática.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
