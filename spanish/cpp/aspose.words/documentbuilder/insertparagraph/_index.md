---
title: "Aspose::Words::DocumentBuilder::InsertParagraph método"
linktitle: "InsertParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertParagraph método. Inserta un salto de párrafo en el documento en C++."
type: docs
weight: 44000
url: /es/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Inserta un salto de párrafo en el documento.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

El nodo de párrafo que acaba de insertarse. Es el mismo nodo que [CurrentParagraph](../get_currentparagraph/).
## Observaciones


Se utiliza el formato de párrafo actual especificado por la propiedad [ParagraphFormat](../get_paragraphformat/).

Divide el párrafo actual en dos. Después de insertar el párrafo, el cursor se coloca al comienzo del nuevo párrafo.

Se lanza una excepción si no es posible insertar un salto de párrafo en la posición actual del cursor.

## Ejemplos



Muestra cómo insertar un párrafo en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// El método "Writeln" finaliza el párrafo después de añadir texto
// y luego inicia una nueva línea, añadiendo un nuevo párrafo.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Ver también

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
