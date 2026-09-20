---
title: "Método Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags método. Obtiene o establece un valor booleano que indica si se debe ignorar el contenido de StructuredDocumentTag. El valor predeterminado es false en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Obtiene o establece un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/). El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Observaciones


Cuando esta opción se establece en **true**, el contenido de [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) se tratará como texto simple.

De lo contrario, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) se procesará como un [Story](../../../aspose.words/story/) independiente y el patrón de reemplazo se buscará por separado para cada [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), de modo que si el patrón cruza un [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), entonces no se realizará el reemplazo para dicho patrón.

## Ejemplos



Muestra cómo ignorar el contenido de las etiquetas durante el reemplazo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Este párrafo contiene SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
