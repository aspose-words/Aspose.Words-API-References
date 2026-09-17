---
title: "Méthode Aspose::Words::Font::get_TextEffect"
linktitle: "get_TextEffect"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_TextEffect. Obtient ou définit l'effet d'animation de la police en C++."
type: docs
weight: 47000
url: /fr/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Obtient ou définit l'effet d'animation de la police.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## Exemples



Montre comment appliquer un effet visuel à une séquence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Les versions antérieures de Microsoft Word ne prennent en charge que les effets d'animation de police.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## Voir aussi

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
