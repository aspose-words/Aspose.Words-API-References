---
title: "Aspose::Words::Document::get_DefaultTabStop méthode"
linktitle: "get_DefaultTabStop"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_DefaultTabStop méthode. Obtient ou définit l'intervalle (en points) entre les tabulations par défaut en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Obtient ou définit l'intervalle (en points) entre les tabulations par défaut.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
