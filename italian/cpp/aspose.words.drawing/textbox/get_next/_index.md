---
title: "Metodo Aspose::Words::Drawing::TextBox::get_Next"
linktitle: "get_Next"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::TextBox::get_Next. Restituisce o imposta un TextBox che rappresenta il TextBox successivo in una sequenza di forme in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing/textbox/get_next/
---
## TextBox::get_Next method


Restituisce o imposta un [TextBox](../) che rappresenta il [TextBox](../) successivo in una sequenza di forme.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::TextBox::get_Next()
```


## Esempi



Mostra come collegare le caselle di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox1 = textBoxShape1->get_TextBox();
builder->Writeln();

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox2 = textBoxShape2->get_TextBox();
builder->Writeln();

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape3 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox3 = textBoxShape3->get_TextBox();
builder->Writeln();

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape4 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox4 = textBoxShape4->get_TextBox();

// Crea collegamenti tra alcune delle caselle di testo.
if (textBox1->IsValidLinkTarget(textBox2))
{
    textBox1->set_Next(textBox2);
}

if (textBox2->IsValidLinkTarget(textBox3))
{
    textBox2->set_Next(textBox3);
}

// Solo una casella di testo vuota può avere un collegamento.
ASSERT_TRUE(textBox3->IsValidLinkTarget(textBox4));

builder->MoveTo(textBoxShape4->get_LastParagraph());
builder->Write(u"Hello world!");

ASSERT_FALSE(textBox3->IsValidLinkTarget(textBox4));

if (textBox1->get_Next() != nullptr && textBox1->get_Previous() == nullptr)
{
    std::cout << "This TextBox is the head of the sequence" << std::endl;
}

if (textBox2->get_Next() != nullptr && textBox2->get_Previous() != nullptr)
{
    std::cout << "This TextBox is the middle of the sequence" << std::endl;
}

if (textBox3->get_Next() == nullptr && textBox3->get_Previous() != nullptr)
{
    std::cout << "This TextBox is the tail of the sequence" << std::endl;

    // Interrompi il collegamento in avanti tra textBox2 e textBox3, quindi verifica che non siano più collegati.
    textBox3->get_Previous()->BreakForwardLink();
    ASSERT_TRUE(textBox2->get_Next() == nullptr);
    ASSERT_TRUE(textBox3->get_Previous() == nullptr);
}

doc->Save(get_ArtifactsDir() + u"Shape.CreateLinkBetweenTextBoxes.docx");
```

## Vedi anche

* Class [TextBox](../)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
