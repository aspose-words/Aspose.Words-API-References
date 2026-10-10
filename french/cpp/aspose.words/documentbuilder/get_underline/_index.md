---
title: "Aspose::Words::DocumentBuilder::get_Underline méthode"
linktitle: "get_Underline"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_Underline méthode. Obtient/definit le type de soulignement pour la police actuelle en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Obtient/définit le type de soulignement pour la police actuelle.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Exemples



Montre comment formater le texte inséré par un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// Le builder applique le formatage à son paragraphe actuel et à tout nouveau texte ajouté par la suite.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## Voir aussi

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
