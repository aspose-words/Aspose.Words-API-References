---
title: "Aspose::Words::Document::get_LayoutOptions método"
linktitle: "get_LayoutOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_LayoutOptions método. Obtiene un objeto LayoutOptions que representa opciones para controlar el proceso de diseño de este documento en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words/document/get_layoutoptions/
---
## Document::get_LayoutOptions method


Obtiene un objeto [LayoutOptions](../../../aspose.words.layout/layoutoptions/) que representa opciones para controlar el proceso de diseño de este documento.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
```


## Ejemplos



Muestra cómo ocultar texto en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte texto oculto, luego especifique si deseamos omitirlo de un documento renderizado.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Muestra cómo mostrar los símbolos de párrafo en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue algunos párrafos, luego habilite los símbolos de párrafo para mostrar los finales de los párrafos
// con un símbolo de párrafo (¶) cuando renderizamos el documento.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Elimine la barra que aparece a la izquierda de cada línea revisada.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ver también

* Class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
