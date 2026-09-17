---
title: "Méthode Aspose::Words::PageSetup::get_TextOrientation"
linktitle: "get_TextOrientation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PageSetup::get_TextOrientation. Permet de spécifier TextOrientation pour toute la page. La valeur par défaut est Horizontal en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Permet de spécifier [TextOrientation](./) pour toute la page. La valeur par défaut est [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Exemples



Montre comment définir l'orientation du texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Définissez la propriété "TextOrientation" sur "TextOrientation.Upward" pour faire pivoter tout le texte de 90 degrés
// vers la droite afin que tout le texte de gauche à droite aille maintenant de haut en bas.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## Voir aussi

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
