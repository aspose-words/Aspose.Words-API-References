---
title: "Classe Aspose::Words::Loading::ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Loading::ResourceLoadingArgs. Fornisce dati per il metodo ResourceLoading() in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Fornisce dati per il metodo [ResourceLoading()](../iresourceloadingcallback/resourceloading/).

```cpp
class ResourceLoadingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | URI originale della risorsa come specificato nel documento importato. |
| [get_ResourceType](./get_resourcetype/)() const | Tipo di risorsa. |
| [get_Uri](./get_uri/)() const | URI della risorsa utilizzato per il download se [ResourceLoading()](../iresourceloadingcallback/resourceloading/) restituisce [Default](../resourceloadingaction/). Inizialmente è impostato sull'URI assoluto della risorsa, ma l'utente può ridefinirlo a qualsiasi valore. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Imposta i dati forniti dall'utente della risorsa che vengono utilizzati se [ResourceLoading()](../iresourceloadingcallback/resourceloading/) restituisce [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
