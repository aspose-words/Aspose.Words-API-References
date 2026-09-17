---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes method"
linktitle: "get_IgnoreShapes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes method. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes dans un texte. La valeur par défaut est false en C++."
type: docs
weight: 11500
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreshapes/
---
## FindReplaceOptions::get_IgnoreShapes method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes à l'intérieur d'un texte. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes() const
```


## Exemples



Montre comment ignorer les formes lors du remplacement de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 200, 200);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder->get_Document()->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
