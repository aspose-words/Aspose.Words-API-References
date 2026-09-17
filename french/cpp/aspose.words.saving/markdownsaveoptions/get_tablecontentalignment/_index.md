---
title: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment"
linktitle: "get_TableContentAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment. Obtient ou définit une valeur qui spécifie comment aligner le contenu des tableaux lors de l'exportation au format Markdown. La valeur par défaut est Auto en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_tablecontentalignment/
---
## MarkdownSaveOptions::get_TableContentAlignment method


Obtient ou définit une valeur qui spécifie comment aligner le contenu des tableaux lors de l'exportation au format [Markdown](../../../aspose.words/saveformat/). La valeur par défaut est [Auto](../../tablecontentalignment/).

```cpp
Aspose::Words::Saving::TableContentAlignment Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment() const
```


## Exemples



Montre comment aligner le contenu dans les tableaux.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_TableContentAlignment(tableContentAlignment);

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

switch (tableContentAlignment)
{
    case Aspose::Words::Saving::TableContentAlignment::Auto:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Left:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Center:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Right:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

}
```

## Voir aussi

* Enum [TableContentAlignment](../../tablecontentalignment/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
