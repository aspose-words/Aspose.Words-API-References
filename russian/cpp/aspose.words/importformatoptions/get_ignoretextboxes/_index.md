---
title: "Метод Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes"
linktitle: "get_IgnoreTextBoxes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes. Получает или задает логическое значение, указывающее, что форматирование содержимого текстовых полей игнорируется, если используется режим KeepSourceFormatting. Значение по умолчанию — true в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


Получает или задает логическое значение, указывающее, что форматирование содержимого текстовых полей игнорируется, если используется режим [KeepSourceFormatting](../../importformatmode/). Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## Примеры



Показывает, как управлять форматированием текстовых полей при добавлении документа.
```cpp
// Создайте документ, в который будут вставлены узлы из другого документа.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// Создайте другой документ с текстовым полем, которое мы импортируем в первый документ.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// Установите флаг, чтобы указать, следует ли очищать или сохранять форматирование текстовых полей
// при их импорте в другие документы.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// Импортируйте текстовое поле из исходного документа в целевой документ,
// а затем проверьте, сохранили ли мы стилизацию его текстового содержимого.
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

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
