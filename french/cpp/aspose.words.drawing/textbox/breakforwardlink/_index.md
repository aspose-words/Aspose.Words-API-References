---
title: "Aspose::Words::Drawing::TextBox::BreakForwardLink méthode"
linktitle: "BreakForwardLink"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBox::BreakForwardLink méthode. Rompt le lien vers la zone de texte suivante en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox::BreakForwardLink method


Rompt le lien vers la prochaine [TextBox](../).

```cpp
void Aspose::Words::Drawing::TextBox::BreakForwardLink()
```


## Exemples



Montre comment lier des zones de texte.
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

// Créez des liens entre certains des zones de texte.
if (textBox1->IsValidLinkTarget(textBox2))
{
    textBox1->set_Next(textBox2);
}

if (textBox2->IsValidLinkTarget(textBox3))
{
    textBox2->set_Next(textBox3);
}

// Seule une zone de texte vide peut avoir un lien.
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

    // Rompez le lien avant entre textBox2 et textBox3, puis vérifiez qu'ils ne sont plus liés.
    textBox3->get_Previous()->BreakForwardLink();
    ASSERT_TRUE(textBox2->get_Next() == nullptr);
    ASSERT_TRUE(textBox3->get_Previous() == nullptr);
}

doc->Save(get_ArtifactsDir() + u"Shape.CreateLinkBetweenTextBoxes.docx");
```

## Voir aussi

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
