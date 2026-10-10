---
title: "Aspose::Words::Drawing::ShadowFormat::get_Transparency metod"
linktitle: "get_Transparency"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShadowFormat::get_Transparency metod. Hämtar eller anger graden av transparens för skuggeffekten som ett värde mellan 0.0 (opak) och 1.0 (klar). Standardvärdet är 0.0 i C++."
type: docs
weight: 2750
url: /sv/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Hämtar eller anger graden av transparens för skuggeffekten som ett värde mellan 0.0 (opak) och 1.0 (klar). Standardvärdet är 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Exempel



Visar hur man ställer in en färg med transparens.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## Se även

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
