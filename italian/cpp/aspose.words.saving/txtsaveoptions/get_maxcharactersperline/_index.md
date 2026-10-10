---
title: "Metodo get_MaxCharactersPerLine della classe Aspose::Words::Saving::TxtSaveOptions."
linktitle: "get_MaxCharactersPerLine"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_MaxCharactersPerLine della classe Aspose::Words::Saving::TxtSaveOptions. Ottiene o imposta un valore intero che specifica il numero massimo di caratteri per una riga. Il valore predefinito è 0, il che significa nessun limite in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Ottiene o imposta un valore intero che specifica il numero massimo di caratteri per una riga. Il valore predefinito è 0, il che significa nessun limite.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Esempi



Mostra come impostare il numero massimo di caratteri per riga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Imposta 30 caratteri come massimo consentito per una riga.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## Vedi anche

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
