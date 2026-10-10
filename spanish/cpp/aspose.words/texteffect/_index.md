---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextEffect enum. Efecto de animación para ejecuciones de texto en C++."
type: docs
weight: 123000
url: /es/cpp/aspose.words/texteffect/
---
## TextEffect enum


Efecto de animación para ejecuciones de texto.

```cpp
enum class TextEffect
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
