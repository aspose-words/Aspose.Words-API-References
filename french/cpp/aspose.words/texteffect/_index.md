---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextEffect enum. Effet d'animation pour les séquences de texte en C++."
type: docs
weight: 123000
url: /fr/cpp/aspose.words/texteffect/
---
## TextEffect enum


Effet d'animation pour les segments de texte.

```cpp
enum class TextEffect
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
