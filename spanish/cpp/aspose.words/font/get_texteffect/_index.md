---
title: "Aspose::Words::Font::get_TextEffect método"
linktitle: "get_TextEffect"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_TextEffect método. Obtiene o establece el efecto de animación de la fuente en C++."
type: docs
weight: 47000
url: /es/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Obtiene o establece el efecto de animación de la fuente.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## Ejemplos



Muestra cómo aplicar un efecto visual a una ejecución.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Las versiones anteriores de Microsoft Word solo admiten efectos de animación de fuentes.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## Ver también

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
