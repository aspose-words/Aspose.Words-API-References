---
title: "Metodo Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes"
linktitle: "get_IgnoreTextBoxes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes. Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo è ignorata se viene usata la modalità KeepSourceFormatting. Il valore predefinito è true in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo è ignorata se viene usata la modalità [KeepSourceFormatting](../../importformatmode/). Il valore predefinito è **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## Esempi



Mostra come gestire la formattazione delle caselle di testo durante l'aggiunta di un documento.
```cpp
// Crea un documento che conterrà i nodi di un altro documento inseriti al suo interno.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// Crea un altro documento con una casella di testo, che importeremo nel primo documento.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// Imposta un flag per specificare se cancellare o preservare la formattazione della casella di testo
// durante l'importazione in altri documenti.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// Importa la casella di testo dal documento di origine nel documento di destinazione,
// e poi verifica se abbiamo conservato lo stile del suo contenuto testuale.
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

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
