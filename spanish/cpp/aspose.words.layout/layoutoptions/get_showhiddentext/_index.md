---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText método"
linktitle: "get_ShowHiddenText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText método. Obtiene o establece la indicación de si el texto oculto en el documento se renderiza. El valor predeterminado es false en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Obtiene o establece la indicación de si se renderiza el texto oculto en el documento. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Ejemplos



Muestra cómo ocultar texto en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte texto oculto, luego especifique si deseamos omitirlo de un documento renderizado.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## Ver también

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
