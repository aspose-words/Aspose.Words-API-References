---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel método"
linktitle: "get_OutlineLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel método. Especifica el nivel de esquema del párrafo en el documento en C++."
type: docs
weight: 26000
url: /es/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Especifica el nivel de esquema del párrafo en el documento.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Ejemplos



Muestra cómo configurar los niveles de esquema de párrafo para crear texto plegable.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cada párrafo tiene un OutlineLevel, que puede ser cualquier número del 1 al 9, o el valor predeterminado "BodyText".
// Establecer la propiedad a uno de los valores numerados mostrará una flecha a la izquierda
// del comienzo del párrafo.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// El nivel 1 es el nivel más alto. Si hay un párrafo con un nivel inferior debajo de un párrafo con un nivel superior,
// colapsar el párrafo de nivel superior colapsará el párrafo de nivel inferior.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Dos párrafos del mismo nivel no colapsarán entre sí,
// y las flechas no colapsan los párrafos a los que apuntan.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// El valor predeterminado "BodyText" es el más bajo, que un párrafo de cualquier nivel puede colapsar.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## Ver también

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
