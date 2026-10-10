---
title: "Champ Aspose::Words::ControlChar::TabChar"
linktitle: "TabChar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Champ Aspose::Words::ControlChar::TabChar. Caractère de tabulation : (char)9 ou \"\\t\" en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Caractère de tabulation : (char)9 ou "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
```


## Exemples



Montre comment définir un intervalle personnalisé pour les positions de tabulation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez les tabulations pour apparaître toutes les 72 points (1 pouce).
builder->get_Document()->set_DefaultTabStop(72);

// Chaque caractère de tabulation ancre le texte qui le suit à la position de tabulation la plus proche suivante.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## Voir aussi

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
