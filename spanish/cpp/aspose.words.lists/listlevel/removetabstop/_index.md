---
title: "Método Aspose::Words::Lists::ListLevel::RemoveTabStop"
linktitle: "RemoveTabStop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Lists::ListLevel::RemoveTabStop. Elimina la tabulación del nivel de lista en C++."
type: docs
weight: 22500
url: /es/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Elimina la tabulación del nivel de lista.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Ejemplos



Muestra cómo borrar la tabulación del nivel de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crear una lista con formato predeterminado
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Obtener el nivel de lista y eliminar su tabulación
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## Ver también

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
