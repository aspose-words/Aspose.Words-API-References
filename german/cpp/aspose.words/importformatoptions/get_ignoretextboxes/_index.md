---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes-Methode"
linktitle: "get_IgnoreTextBoxes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes-Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der KeepSourceFormatting‑Modus verwendet wird. Der Standardwert ist true in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der Modus [KeepSourceFormatting](../../importformatmode/) verwendet wird. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## Beispiele



Zeigt, wie die Formatierung von Textfeldern beim Anhängen eines Dokuments verwaltet wird.
```cpp
// Erstellen Sie ein Dokument, in das Knoten aus einem anderen Dokument eingefügt werden.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// Erstellen Sie ein weiteres Dokument mit einem Textfeld, das wir in das erste Dokument importieren.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// Setzen Sie ein Flag, um festzulegen, ob die Textfeldformatierung gelöscht oder beibehalten werden soll
// während sie in andere Dokumente importiert werden.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// Importieren Sie das Textfeld vom Quelldokument in das Zieldokument,
// und prüfen Sie anschließend, ob wir die Formatierung seines Textinhalts beibehalten haben.
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

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
