---
title: "Aspose::Words::TextDmlEffect enumeración"
linktitle: "TextDmlEffect"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::TextDmlEffect. Efecto de texto Dml para ejecuciones de texto en C++."
type: docs
weight: 122000
url: /es/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Efecto de texto Dml para ejecuciones de texto.

```cpp
enum class TextDmlEffect
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Glow | 0 | Efecto de resplandor, en el que se agrega un contorno difuminado de color fuera de los bordes del objeto. |
| Fill | 1 | Efecto de superposición de relleno. |
| Shadow | 2 | Efecto de sombra. |
| Outline | 3 | Efecto de contorno. |
| Effect3D | 4 | Efecto 3D. |
| Reflection | 5 | Efecto de reflejo. |


## Ejemplos



Muestra cómo comprobar si una ejecución muestra un efecto de texto DrawingML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
