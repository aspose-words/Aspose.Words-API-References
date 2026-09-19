---
title: "Metodo Aspose::Words::Drawing::ShadowFormat::get_Color"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShadowFormat::get_Color. Ottiene o imposta un oggetto Color che rappresenta il colore dell'ombra. Il valore predefinito è Nero in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.drawing/shadowformat/get_color/
---
## ShadowFormat::get_Color method


Ottiene o imposta un oggetto **Color** che rappresenta il colore dell'ombra. Il valore predefinito è **Black**.

```cpp
System::Drawing::Color Aspose::Words::Drawing::ShadowFormat::get_Color()
```


## Esempi



Mostra come ottenere il colore dell'ombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```


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
