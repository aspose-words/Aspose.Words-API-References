---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer metodo"
linktitle: "GetMathRenderer"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer metodo. Crea e restituisce un oggetto che può essere usato per renderizzare questa equazione in un'immagine in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Crea e restituisce un oggetto che può essere usato per renderizzare questa equazione in un'immagine.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

L'oggetto renderer per questa equazione.
## Note


Questo metodo invoca semplicemente il costruttore di [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) e passa questo oggetto come parametro.

## Esempi



Mostra come renderizzare un oggetto Office [Math](../../) in un file immagine nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Crea un oggetto "ImageSaveOptions" da passare al metodo "Save" del renderer del nodo per modificare
// come renderizza il nodo OfficeMath in un'immagine.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Imposta la proprietà "Scale" a 5 per renderizzare l'oggetto a cinque volte la sua dimensione originale.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Vedi anche

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
