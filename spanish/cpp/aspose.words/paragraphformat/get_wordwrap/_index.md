---
title: "Método Aspose::Words::ParagraphFormat::get_WordWrap"
linktitle: "get_WordWrap"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ParagraphFormat::get_WordWrap. Si esta propiedad es false, el texto latino en medio de una palabra puede dividirse en el párrafo actual. De lo contrario, el texto latino se envuelve por palabras completas en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Si esta propiedad es **false**, el texto latino en medio de una palabra puede dividirse en el párrafo actual. De lo contrario, el texto latino se divide por palabras completas.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
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
