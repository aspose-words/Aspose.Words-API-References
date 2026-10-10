---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode énum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode énum. Spécifie comment Aspose.Words exporte les paragraphes vides vers Markdown en C++."
type: docs
weight: 66250
url: /fr/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Spécifie comment Aspose.Words exporte les paragraphes vides vers Markdown.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| EmptyLine | 0 | Exporter sous forme de lignes vides. |
| MarkdownHardLineBreak | 1 | Exporter le caractère de saut de ligne dur Markdown '\\'. |
| None | 2 | Ne pas exporter les paragraphes vides. |


## Exemples



Montre comment exporter les paragraphes vides.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"First");
builder->Writeln(u"\r\n\r\n\r\n");
builder->Writeln(u"Last");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_EmptyParagraphExportMode(exportMode);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

System::String result = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.EmptyParagraphExportMode.md");

switch (exportMode)
{
    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::None:
        ASSERT_EQ(u"First\r\n\r\nLast\r\n", result);
        break;

    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::EmptyLine:
        ASSERT_EQ(u"First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;

    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::MarkdownHardLineBreak:
        ASSERT_EQ(u"First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;

}
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
