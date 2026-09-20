---
title: "Aspose::Words::SectionCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::SectionCollection::idx_get método. Recupera una sección en el índice dado en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


Recupera una sección en el índice dado.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la lista de secciones. |
## Observaciones


El índice comienza en cero.

Se permiten índices negativos e indican acceso desde el final de la colección. Por ejemplo, -1 significa el último elemento, -2 el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos en la lista, esto devuelve una referencia nula.

## Ejemplos



Muestra cuándo recalcular el diseño de página del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez lo hará automáticamente
// almacenar en caché el diseño del documento dentro de sus páginas.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifique el documento de alguna manera.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// En la versión actual de Aspose.Words, modificar el documento no vuelve a reconstruir automáticamente
// el diseño de página en caché. Si deseamos que el diseño en caché
// se mantenga actualizado, necesitaremos actualizarlo manualmente.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```


Muestra cómo preparar un nuevo nodo de sección para editar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco viene con una sección, que tiene un cuerpo, que a su vez tiene un párrafo.
// Podemos agregar contenido a este documento añadiendo elementos como ejecuciones de texto, formas o tablas a ese párrafo.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Si añadimos una nueva sección de esta manera, no tendrá un cuerpo ni ningún otro nodo hijo.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Ejecute el método \"EnsureMinimum\" para agregar un cuerpo y un párrafo a esta sección y comenzar a editarla.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
