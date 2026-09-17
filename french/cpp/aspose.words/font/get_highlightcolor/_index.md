---
title: "Aspose::Words::Font::get_HighlightColor méthode"
linktitle: "get_HighlightColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_HighlightColor méthode. Obtient ou définit la couleur de surbrillance (marqueur) en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Obtient ou définit la couleur de surbrillance (marqueur).

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Exemples



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
