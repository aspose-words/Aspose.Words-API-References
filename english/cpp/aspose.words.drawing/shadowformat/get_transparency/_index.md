---
title: Aspose::Words::Drawing::ShadowFormat::get_Transparency method
linktitle: get_Transparency
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShadowFormat::get_Transparency method. Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0 in C++.'
type: docs
weight: 2750
url: /cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Examples



Shows how to set a color with transparency. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## See Also

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
