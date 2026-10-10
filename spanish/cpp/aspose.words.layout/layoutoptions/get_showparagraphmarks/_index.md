---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks método"
linktitle: "get_ShowParagraphMarks"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks método. Obtiene o establece la indicación de si se renderizan las marcas de párrafo. El valor predeterminado es false en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Obtiene o establece la indicación de si se renderizan los símbolos de párrafo. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Ejemplos



Muestra cómo mostrar los símbolos de párrafo en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue algunos párrafos, luego habilite los símbolos de párrafo para mostrar los finales de los párrafos
// con un símbolo de párrafo (¶) cuando renderizamos el documento.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## Ver también

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
