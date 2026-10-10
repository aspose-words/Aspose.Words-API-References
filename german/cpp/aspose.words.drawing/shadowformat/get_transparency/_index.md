---
title: "Aspose::Words::Drawing::ShadowFormat::get_Transparency Methode"
linktitle: "get_Transparency"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShadowFormat::get_Transparency Methode. Liest oder setzt den Grad der Transparenz für den Schatteneffekt als Wert zwischen 0,0 (undurchsichtig) und 1,0 (klar). Der Standardwert ist 0,0 in C++."
type: docs
weight: 2750
url: /de/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Liest oder setzt den Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent). Der Standardwert ist 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Beispiele



Zeigt, wie man eine Farbe mit Transparenz festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## Siehe auch

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
