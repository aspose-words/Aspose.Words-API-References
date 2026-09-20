---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents método"
linktitle: "get_MirrorIndents"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ParagraphFormat::get_MirrorIndents. Obtiene o establece una bandera que indica si los sangrados izquierdo y derecho tienen la misma anchura en C++."
type: docs
weight: 24500
url: /es/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Obtiene o establece una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Ejemplos



Muestra cómo hacer que los sangrados izquierdo y derecho sean iguales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
