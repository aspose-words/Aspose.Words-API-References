---
title: "Aspose::Words::Comment::get_StoryType método"
linktitle: "get_StoryType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::get_StoryType método. Devuelve Comments en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/comment/get_storytype/
---
## Comment::get_StoryType method


Devuelve [Comments](../../storytype/).

```cpp
Aspose::Words::StoryType Aspose::Words::Comment::get_StoryType() override
```


## Ejemplos



Muestra cómo insertar nodos [InlineStory](../../inlinestory/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// Los nodos de tabla tienen un método \"EnsureMinimum()\" que asegura que la tabla tenga al menos una celda.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Podemos colocar una tabla dentro de una nota al pie, lo que hará que aparezca en el pie de página de la página de referencia.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// Un InlineStory también tiene un método \"EnsureMinimum()\", pero en este caso,
// se asegura de que el último hijo del nodo sea un párrafo,
// para que podamos hacer clic y escribir texto fácilmente en Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Edite la apariencia del ancla, que es el pequeño número en superíndice
// en el texto principal que apunta a la nota al pie.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Todos los nodos de historia en línea tienen sus respectivos tipos de historia.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// Un comentario es otro tipo de historia en línea.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// El párrafo principal de un nodo de historia en línea será el del cuerpo principal del documento.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Sin embargo, el último párrafo es el del contenido de texto del comentario,
// que estará fuera del cuerpo principal del documento en un globo de texto.
// Un comentario no tendrá nodos hijos por defecto,
// por lo que podemos aplicar el método EnsureMinimum() para colocar un párrafo aquí también.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Una vez que tengamos un párrafo, podemos mover el builder para hacerlo y escribir nuestro comentario.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## Ver también

* Enum [StoryType](../../storytype/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
