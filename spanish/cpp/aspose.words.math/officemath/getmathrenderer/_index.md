---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer método"
linktitle: "GetMathRenderer"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer método. Crea y devuelve un objeto que puede usarse para renderizar esta ecuación en una imagen en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Crea y devuelve un objeto que puede usarse para renderizar esta ecuación en una imagen.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

El objeto renderizador para esta ecuación.
## Observaciones


Este método simplemente invoca el constructor de [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) y pasa este objeto como parámetro.

## Ejemplos



Muestra cómo renderizar un objeto Office [Math](../../) en un archivo de imagen en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Cree un objeto "ImageSaveOptions" para pasar al método "Save" del renderizador de nodos y modificar
// cómo renderiza el nodo OfficeMath en una imagen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Establezca la propiedad "Scale" a 5 para renderizar el objeto a cinco veces su tamaño original.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Ver también

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
