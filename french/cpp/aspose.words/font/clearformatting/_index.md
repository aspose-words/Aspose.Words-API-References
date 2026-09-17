---
title: "Méthode Aspose::Words::Font::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::ClearFormatting. Réinitialise le formatage de police par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Réinitialise le formatage de police par défaut.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Remarques


Supprime tout le formatage de police spécifié explicitement sur l'objet à partir duquel [Font](../) a été obtenu afin que le formatage de police soit hérité du parent approprié.

## Exemples



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
