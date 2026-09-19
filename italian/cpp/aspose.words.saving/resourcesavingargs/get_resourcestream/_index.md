---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream metodo"
linktitle: "get_ResourceStream"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream metodo. Consente di specificare lo stream in cui la risorsa verrà salvata in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Consente di specificare il flusso in cui la risorsa verrà salvata.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Note


Questa proprietà consente di salvare le risorse su stream invece che su file.

Il valore predefinito è **null**. Quando questa proprietà è **null**, la risorsa verrà salvata in un file specificato nella proprietà [ResourceFileName](../get_resourcefilename/).

Utilizzando [IResourceSavingCallback](../../iresourcesavingcallback/) non è possibile sostituire una risorsa con un'altra. È destinato solo al controllo della posizione in cui salvare le risorse.

## Vedi anche

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
