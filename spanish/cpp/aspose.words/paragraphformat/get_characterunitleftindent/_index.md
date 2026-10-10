---
title: "Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent método"
linktitle: "get_CharacterUnitLeftIndent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent método. Obtiene o establece el valor de sangría izquierda (en caracteres) para los párrafos especificados en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/paragraphformat/get_characterunitleftindent/
---
## ParagraphFormat::get_CharacterUnitLeftIndent method


Obtiene o establece el valor de sangría izquierda (en caracteres) para los párrafos especificados.

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent()
```


## Ejemplos



Muestra cómo cambiar el espaciado y las sangrías de los párrafos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// A continuación se presentan cinco opciones de espaciado diferentes, junto con las propiedades que su configuración afecta indirectamente.
// 1 -  Sangría izquierda:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Sangría derecha:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Sangría colgante:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Interlineado antes de los párrafos:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Interlineado después de los párrafos:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
