---
title: "Aspose::Words::ControlChar::PageBreak método"
linktitle: "PageBreak"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ControlChar::PageBreak método. Carácter de salto de página: \"\\x000c\" o \"\\f\". Nota que tiene el mismo valor que SectionBreak en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/controlchar/pagebreak/
---
## ControlChar::PageBreak method


Carácter de salto de página: "\x000c" o "\f". Nota que tiene el mismo valor que [SectionBreak](../sectionbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::PageBreak()
```


## Ejemplos



Muestra cómo agregar varios caracteres de control a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregar un espacio regular.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::SpaceChar + u"After space.");

// Agregar un NBSP, que es un espacio de no separación.
// A diferencia del espacio regular, este espacio no puede tener un salto de línea automático en su posición.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::NonBreakingSpace() + u"After space.");

// Agregar un carácter de tabulación.
builder->Write(System::String(u"Before tab.") + Aspose::Words::ControlChar::Tab() + u"After tab.");

// Agregar un salto de línea.
builder->Write(System::String(u"Before line break.") + Aspose::Words::ControlChar::LineBreak() + u"After line break.");

// Agregar una nueva línea y comienza un nuevo párrafo.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());
builder->Write(System::String(u"Before line feed.") + Aspose::Words::ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// El carácter de salto de línea tiene dos versiones.
ASSERT_EQ(Aspose::Words::ControlChar::LineFeed(), Aspose::Words::ControlChar::Lf());

// Los retornos de carro y los saltos de línea pueden representarse juntos con un solo carácter.
ASSERT_EQ(Aspose::Words::ControlChar::CrLf(), Aspose::Words::ControlChar::Cr() + Aspose::Words::ControlChar::Lf());

// Agregar un salto de párrafo, que iniciará un nuevo párrafo.
builder->Write(System::String(u"Before paragraph break.") + Aspose::Words::ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(3, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Agregar un salto de sección. Esto no crea una nueva sección ni un nuevo párrafo.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
builder->Write(System::String(u"Before section break.") + Aspose::Words::ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Agregar un salto de página.
builder->Write(System::String(u"Before page break.") + Aspose::Words::ControlChar::PageBreak() + u"After page break.");

// Un salto de página tiene el mismo valor que un salto de sección.
ASSERT_EQ(Aspose::Words::ControlChar::PageBreak(), Aspose::Words::ControlChar::SectionBreak());

// Insertar una nueva sección y luego establecer su recuento de columnas a dos.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// Podemos usar un carácter de control para marcar el punto donde el texto pasa a la siguiente columna.
builder->Write(System::String(u"Text at end of column 1.") + Aspose::Words::ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(get_ArtifactsDir() + u"ControlChar.InsertControlChars.docx");

// Existen contrapartes de tipo char y string para la mayoría de los caracteres.
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Cell()), Aspose::Words::ControlChar::CellChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::NonBreakingSpace()), Aspose::Words::ControlChar::NonBreakingSpaceChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Tab()), Aspose::Words::ControlChar::TabChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineBreak()), Aspose::Words::ControlChar::LineBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineFeed()), Aspose::Words::ControlChar::LineFeedChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ParagraphBreak()), Aspose::Words::ControlChar::ParagraphBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::SectionBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::PageBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ColumnBreak()), Aspose::Words::ControlChar::ColumnBreakChar);
```

## Ver también

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
