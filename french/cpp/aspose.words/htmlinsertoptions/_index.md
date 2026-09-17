---
title: "Énumération Aspose::Words::HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::HtmlInsertOptions enum. Spécifie les options pour la méthode InsertHtml() en C++."
type: docs
weight: 92000
url: /fr/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Spécifie les options pour la méthode [InsertHtml()](../).

```cpp
enum class HtmlInsertOptions
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Utilisez les options par défaut lors de l’insertion de HTML. |
| UseBuilderFormatting | 1 | Utilisez la mise en forme de police et de paragraphe spécifiée dans [DocumentBuilder](../documentbuilder/) comme mise en forme de base pour le texte inséré depuis le HTML. |
| RemoveLastEmptyParagraph | 2 | Supprime le paragraphe vide qui est normalement inséré après un HTML se terminant par un élément de niveau bloc. |
| PreserveBlocks | 4 | Préserve les propriétés des éléments de niveau bloc. |


## Exemples



Montre comment permettre une meilleure préservation des bordures et des marges observées.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Définissez le nouveau mode d'importation des éléments de niveau bloc HTML.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
