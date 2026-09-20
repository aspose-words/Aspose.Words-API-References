---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement método"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement método. Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente. El valor predeterminado es false en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Ejemplos



Muestra cómo eliminar un párrafo de una celda de tabla con una tabla anidada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree una tabla con párrafo y tabla interna en la primera celda.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// Cuando la siguiente opción se establece en 'true', Aspose.Words eliminará el texto del párrafo
// completamente junto con su marca de párrafo. De lo contrario, Aspose.Words imitará a Word y eliminará
// solo el texto del párrafo y dejará la marca de párrafo intacta (cuando una tabla sigue al texto).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
