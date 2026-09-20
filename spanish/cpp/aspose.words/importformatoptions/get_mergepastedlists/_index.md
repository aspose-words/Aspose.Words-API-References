---
title: "Método Aspose::Words::ImportFormatOptions::get_MergePastedLists"
linktitle: "get_MergePastedLists"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ImportFormatOptions::get_MergePastedLists. Obtiene o establece un valor booleano que especifica si las listas pegadas se combinarán con las listas circundantes. El valor predeterminado es false en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Obtiene o establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Ejemplos



Muestra cómo combinar listas de un documento.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Establezca la propiedad "MergePastedLists" a "true" para que las listas pegadas se combinen con las listas circundantes.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
