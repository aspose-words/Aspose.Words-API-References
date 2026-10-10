---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes méthode"
linktitle: "get_IgnoreTextBoxes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes méthode. Obtient ou définit une valeur booléenne qui indique que le formatage source du contenu des zones de texte est ignoré si le mode KeepSourceFormatting est utilisé. La valeur par défaut est true en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


Obtient ou définit une valeur booléenne qui indique que le formatage source du contenu des zones de texte est ignoré si le mode [KeepSourceFormatting](../../importformatmode/) est utilisé. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## Exemples



Montre comment gérer le formatage des zones de texte lors de l'ajout d'un document.
```cpp
// Créez un document dans lequel les nœuds d'un autre document seront insérés.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// Créez un autre document avec une zone de texte, que nous importerons dans le premier document.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// Définissez un indicateur pour spécifier s'il faut effacer ou préserver le formatage des zones de texte
// lors de leur importation dans d'autres documents.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// Importez la zone de texte du document source dans le document de destination,
// et vérifiez ensuite si nous avons conservé le style de son contenu texte.
auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);
auto importedTextBox = System::ExplicitCast<Aspose::Words::Drawing::Shape>(importer->ImportNode(textBox, true));
dstDoc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedTextBox);

if (ignoreTextBoxes)
{
    ASPOSE_ASSERT_EQ(12.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Times New Roman", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}
else
{
    ASPOSE_ASSERT_EQ(24.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Courier New", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.IgnoreTextBoxes.docx");
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
