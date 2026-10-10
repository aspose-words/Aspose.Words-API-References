---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation método"
linktitle: "get_HangingPunctuation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation método. Obtiene o establece una bandera que indica si la puntuación colgante está habilitada para el párrafo actual en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Obtiene o establece una bandera que indica si la puntuación colgante está habilitada para el párrafo actual.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
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
