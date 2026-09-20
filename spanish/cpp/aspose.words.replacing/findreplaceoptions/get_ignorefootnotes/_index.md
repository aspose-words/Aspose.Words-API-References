---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes método"
linktitle: "get_IgnoreFootnotes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes. Obtiene o establece un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es false en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Obtiene o establece un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Ejemplos



Muestra cómo ignorar las notas al pie durante una operación de buscar y reemplazar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Establezca la bandera "IgnoreFootnotes" a "true" para obtener la operación de buscar y reemplazar
// operación para ignorar el texto dentro de las notas al pie.
// Establezca la bandera "IgnoreFootnotes" a "false" para obtener la operación de buscar y reemplazar
// operación para también buscar texto dentro de las notas al pie.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
