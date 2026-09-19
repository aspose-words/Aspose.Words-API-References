---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri metodo"
linktitle: "get_ResourceFileUri"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri metodo. Ottiene o imposta l'identificatore uniforme di risorsa (URI) utilizzato per fare riferimento al file di risorsa dal documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


Ottiene o imposta l'identificatore uniforme di risorsa (URI) utilizzato per fare riferimento al file della risorsa dal documento.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## Note


Questa proprietà consente di modificare gli URI dei file di risorsa esportati in documenti HTML a pagina fissa, SVG o Markdown.

Aspose.Words genera automaticamente un URI per ogni file di risorsa durante l'esportazione in formato HTML a pagina fissa, SVG o Markdown. Gli URI generati fanno riferimento ai file di risorsa salvati da Aspose.Words. Tuttavia, gli URI possono essere errati se i file di risorsa vengono spostati in un'altra posizione o se i file di risorsa sono salvati su stream. Questa proprietà consente di correggere gli URI in questi casi.

Quando l'evento viene attivato, questa proprietà contiene l'URI generato da Aspose.Words. È possibile modificare il valore di questa proprietà per fornire un URI personalizzato per il file di risorsa.
## Vedi anche

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
