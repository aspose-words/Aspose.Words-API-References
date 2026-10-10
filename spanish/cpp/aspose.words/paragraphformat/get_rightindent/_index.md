---
title: "Aspose::Words::ParagraphFormat::get_RightIndent método"
linktitle: "get_RightIndent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_RightIndent método. Obtiene o establece el valor (en puntos) que representa la sangría derecha para el párrafo en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words/paragraphformat/get_rightindent/
---
## ParagraphFormat::get_RightIndent method


Obtiene o establece el valor (en puntos) que representa la sangría derecha del párrafo.

```cpp
double Aspose::Words::ParagraphFormat::get_RightIndent()
```


## Ejemplos



Muestra cómo configurar el formato de párrafo para crear texto descentrado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Centrar todo el texto que escribe el generador de documentos y configurar sangrías.
// La configuración de sangría a continuación creará un bloque de texto que quedará asimétricamente en la página.
// El "centro" al que alineamos el texto será el medio del cuerpo del texto, no el medio de la página.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
