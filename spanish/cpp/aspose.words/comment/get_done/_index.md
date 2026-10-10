---
title: "Aspose::Words::Comment::get_Done método"
linktitle: "get_Done"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::get_Done método. Obtiene o establece la bandera que indica que el comentario ha sido marcado como completado en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Obtiene o establece la bandera que indica que el comentario ha sido marcado como completado.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Ejemplos



Muestra cómo marcar un comentario como "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Inserte un comentario para señalar un error.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Los comentarios tienen una bandera "Done", que se establece en "false" por defecto.
// Si un comentario sugiere que hagamos un cambio dentro del documento,
// podemos aplicar el cambio y luego también establecer la bandera "Done" después para indicar la corrección.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Los comentarios que están "done" se diferenciarán
// de los que no están "hecho" con un color de texto desvanecido.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Ver también

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
