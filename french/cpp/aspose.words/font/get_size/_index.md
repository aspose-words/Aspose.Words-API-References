---
title: "Méthode Aspose::Words::Font::get_Size"
linktitle: "get_Size"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Size. Obtient ou définit la taille de la police en points en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words/font/get_size/
---
## Font::get_Size method


Obtient ou définit la taille de la police en points.

```cpp
double Aspose::Words::Font::get_Size()
```


## Exemples



Montre comment insérer du texte formaté en utilisant [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Spécifiez le formatage de la police, puis ajoutez du texte.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


Montre comment formater une séquence de texte en utilisant sa propriété de police.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
