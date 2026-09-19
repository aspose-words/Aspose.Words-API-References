---
title: "Metodo Aspose::Words::Saving::PclSaveOptions::AddPrinterFont"
linktitle: "AddPrinterFont"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PclSaveOptions::AddPrinterFont. Aggiunge informazioni sul carattere che viene caricato nella stampante dal produttore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Aggiunge informazioni sul font che viene caricato nella stampante dal produttore.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFullName | const System::String\& | Nome completo del carattere (ad es. "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Nome del carattere utilizzato nel documento Pcl. |

## Esempi



Mostra come far sì che una stampante sostituisca tutte le occorrenze di un carattere specifico con un carattere diverso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// Durante la stampa di questo documento, la stampante utilizzerà il carattere "Courier New"
// per accedere alle parti in cui il nostro documento ha utilizzato il carattere "Courier".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## Vedi anche

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
