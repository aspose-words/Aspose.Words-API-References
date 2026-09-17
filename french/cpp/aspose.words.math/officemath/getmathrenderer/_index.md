---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer méthode"
linktitle: "GetMathRenderer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer méthode. Crée et renvoie un objet pouvant être utilisé pour rendre cette équation en image en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Crée et renvoie un objet pouvant être utilisé pour rendre cette équation sous forme d’image.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

L'objet de rendu pour cette équation.
## Remarques


Cette méthode invoque simplement le constructeur de [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) et passe cet objet en paramètre.

## Exemples



Montre comment rendre un objet Office [Math](../../) en fichier image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Créez un objet "ImageSaveOptions" à transmettre à la méthode "Save" du rendu de nœud pour modifier
// la façon dont il rend le nœud OfficeMath en image.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Définissez la propriété "Scale" à 5 pour rendre l'objet à cinq fois sa taille originale.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Voir aussi

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
