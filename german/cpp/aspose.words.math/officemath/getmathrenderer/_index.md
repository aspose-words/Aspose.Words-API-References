---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer-Methode"
linktitle: "GetMathRenderer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer method. Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Gleichung in ein Bild in C++ zu rendern."
type: docs
weight: 9000
url: /de/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Gleichung in ein Bild zu rendern.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

Das Renderer-Objekt für diese Gleichung.
## Hinweise


Diese Methode ruft lediglich den Konstruktor von [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) auf und übergibt dieses Objekt als Parameter.

## Beispiele



Zeigt, wie man ein Office [Math](../../)-Objekt in eine Bilddatei im lokalen Dateisystem rendert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Erstellen Sie ein "ImageSaveOptions"-Objekt, um es an die "Save"-Methode des Knoten-Renderers zu übergeben, um zu ändern
// wie es den OfficeMath-Knoten in ein Bild rendert.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Setzen Sie die Eigenschaft "Scale" auf 5, um das Objekt fünfmal so groß wie die Originalgröße zu rendern.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Siehe auch

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
