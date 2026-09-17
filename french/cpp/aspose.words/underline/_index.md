---
title: "Aspose::Words::Underline enum"
linktitle: "Soulignement"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Underline enum. Indique le type de soulignement appliqué à une police en C++."
type: docs
weight: 126000
url: /fr/cpp/aspose.words/underline/
---
## Underline enum


Indique le type de soulignement appliqué à une police.

```cpp
enum class Underline
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 |  |
| Simple | 1 |  |
| Words | 2 |  |
| Double | 3 |  |
| Pointillé | 4 |  |
| Épais | 6 |  |
| Tiret | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Ondulé | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
