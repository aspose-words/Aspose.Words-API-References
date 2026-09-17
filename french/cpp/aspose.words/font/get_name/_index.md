---
title: "Méthode Aspose::Words::Font::get_Name"
linktitle: "get_Name"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Name. Obtient ou définit le nom de la police en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words/font/get_name/
---
## Font::get_Name method


Obtient ou définit le nom de la police.

```cpp
System::String Aspose::Words::Font::get_Name()
```

## Remarques


Lors de la récupération, renvoie [NameAscii](../get_nameascii/).

Lors de la définition, définit [NameAscii](../get_nameascii/), [NameBi](../get_namebi/), [NameFarEast](../get_namefareast/) et [NameOther](../get_nameother/) à la valeur spécifiée.

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
