---
title: "Método Aspose::Words::Drawing::ShadowFormat::get_Transparency"
linktitle: "get_Transparency"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShadowFormat::get_Transparency. Obtiene o establece el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). El valor predeterminado es 0.0 en C++."
type: docs
weight: 2750
url: /es/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Obtiene o establece el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). El valor predeterminado es 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Ejemplos



Muestra cómo establecer un color con transparencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## Ver también

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
