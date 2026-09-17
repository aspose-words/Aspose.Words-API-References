---
title: "Aspose::Words::Font::get_Color méthode"
linktitle: "get_Color"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Color méthode. Obtient ou définit la couleur de la police en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


Obtient ou définit la couleur de la police.

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
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


Montre comment insérer un champ de lien hypertexte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Insérez un lien hypertexte et mettez‑le en évidence avec un formatage personnalisé.
// Le lien hypertexte sera un morceau de texte cliquable qui nous mènera à l'emplacement spécifié dans l'URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic gauche sur le lien dans le texte dans Microsoft Word nous amènera à l'URL via une nouvelle fenêtre de navigateur web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
