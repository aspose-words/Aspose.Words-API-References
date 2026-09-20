---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::CommentDisplayMode enum. Especifica el modo de renderizado para los comentarios del documento en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Especifica el modo de renderizado para los comentarios del documento.

```cpp
enum class CommentDisplayMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Hide | 0 | No se renderizan comentarios del documento. |
| ShowInBalloons | 1 | Renderiza los comentarios del documento en globos en el margen. Este es el valor predeterminado. |
| ShowInAnnotations | 2 | Renderiza los comentarios del documento en anotaciones. Esto solo está disponible para el formato Pdf. |


## Ejemplos



Muestra cómo mostrar los comentarios al guardar un documento en un formato renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations solo está disponible en los formatos Pdf1.7 y Pdf1.5.
// En otros formatos, funcionará de manera similar a Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Tenga en cuenta que es necesario reconstruir el diseño de página del documento (mediante el método Document.UpdatePageLayout()).
// después de cambiar los valores de Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## Ver también

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
