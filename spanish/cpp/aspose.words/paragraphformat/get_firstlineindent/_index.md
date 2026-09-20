---
title: "Método Aspose::Words::ParagraphFormat::get_FirstLineIndent"
linktitle: "get_FirstLineIndent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ParagraphFormat::get_FirstLineIndent. Obtiene o establece el valor (en puntos) para una sangría de primera línea o colgante. Use valores positivos para establecer la sangría de primera línea y valores negativos para establecer la sangría colgante en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Obtiene o establece el valor (en puntos) para una sangría de primera línea o colgante. Use valores positivos para establecer la sangría de primera línea y valores negativos para establecer la sangría colgante.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
