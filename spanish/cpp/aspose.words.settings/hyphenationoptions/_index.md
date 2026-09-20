---
title: "Clase Aspose::Words::Settings::HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Settings::HyphenationOptions. Permite configurar las opciones de guionado del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Permite configurar opciones de guionización del documento. Para obtener más información, visite el artículo de documentación [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Obtiene o establece el valor que determina si el guionado automático está activado para el documento. El valor predeterminado de esta propiedad es **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Obtiene o establece el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Obtiene o establece el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. El valor predeterminado para esta propiedad es **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Obtiene o establece la distancia en 1/20 de punto desde el margen derecho dentro de la cual no se desea dividir palabras con guiones. El valor predeterminado para esta propiedad es 360 (0,25 pulgadas). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Método setter para [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Método setter para [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Método setter para [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Método setter para [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo configurar la división automática de palabras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
