---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShadowFormat class. Rappresenta la formattazione dell'ombra per un oggetto. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Rappresenta la formattazione dell'ombra per un oggetto. Per saperne di più, visita l'articolo di documentazione [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class ShadowFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Cancella la formattazione dell'ombra. |
| [get_Color](./get_color/)() | Ottiene o imposta un oggetto **Color** che rappresenta il colore dell'ombra. Il valore predefinito è **Black**. |
| [get_Transparency](./get_transparency/)() | Ottiene o imposta il grado di trasparenza dell'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0. |
| [get_Type](./get_type/)() | Ottiene o imposta il [ShadowType](../shadowtype/) specificato per [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Restituisce **true** se la formattazione applicata a questa istanza è visibile. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Impostatore per [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Impostatore per [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come ottenere il colore dell'ombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
