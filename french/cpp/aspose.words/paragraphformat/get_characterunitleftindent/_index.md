---
title: "Méthode Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent"
linktitle: "get_CharacterUnitLeftIndent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent. Obtient ou définit la valeur du retrait gauche (en caractères) pour les paragraphes spécifiés en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/paragraphformat/get_characterunitleftindent/
---
## ParagraphFormat::get_CharacterUnitLeftIndent method


Obtient ou définit la valeur du retrait gauche (en caractères) pour les paragraphes spécifiés.

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent()
```


## Exemples



Montre comment modifier l'espacement des paragraphes et les retraits.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Ci-dessous cinq options d'espacement différentes, ainsi que les propriétés que leur configuration affecte indirectement.
// 1 -  Retrait gauche :
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Retrait droit :
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Retrait suspendu :
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Interligne avant les paragraphes :
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Interligne après les paragraphes :
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
