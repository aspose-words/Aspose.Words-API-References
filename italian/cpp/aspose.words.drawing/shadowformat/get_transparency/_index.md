---
title: "Metodo Aspose::Words::Drawing::ShadowFormat::get_Transparency"
linktitle: "get_Transparency"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShadowFormat::get_Transparency. Ottiene o imposta il grado di trasparenza per l'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0 in C++."
type: docs
weight: 2750
url: /it/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Ottiene o imposta il grado di trasparenza dell'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Esempi



Mostra come impostare un colore con trasparenza.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## Vedi anche

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
