---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer metod"
linktitle: "GetMathRenderer"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer metod. Skapar och returnerar ett objekt som kan användas för att rendera denna ekvation till en bild i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Skapar och returnerar ett objekt som kan användas för att rendera denna ekvation till en bild.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

Renderingsobjektet för denna ekvation.
## Anmärkningar


Denna metod anropar bara [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) konstruktorn och skickar detta objekt som en parameter.

## Exempel



Visar hur man renderar ett Office [Math](../../) objekt till en bildfil i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att modifiera
// hur den renderar OfficeMath-noden till en bild.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Ställ in egenskapen "Scale" till 5 för att rendera objektet till fem gånger dess ursprungliga storlek.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Se även

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
