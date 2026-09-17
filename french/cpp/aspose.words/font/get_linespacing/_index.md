---
title: "Méthode Aspose::Words::Font::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_LineSpacing. Retourne l'interligne de cette police (en points) en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Renvoie l'interligne de cette police (en points).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Exemples



Montre comment obtenir l'interligne d'une police, en points.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez différentes polices pour le DocumentBuilder et vérifiez leur interligne.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
