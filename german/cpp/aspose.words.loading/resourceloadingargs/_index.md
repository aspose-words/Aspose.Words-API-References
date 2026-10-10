---
title: "Aspose::Words::Loading::ResourceLoadingArgs Klasse"
linktitle: "ResourceLoadingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::ResourceLoadingArgs Klasse. Stellt Daten für die Methode ResourceLoading() in C++ bereit."
type: docs
weight: 7000
url: /de/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Stellt Daten für die [ResourceLoading()](../iresourceloadingcallback/resourceloading/) Methode bereit.

```cpp
class ResourceLoadingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | Original-URI der Ressource, wie im importierten Dokument angegeben. |
| [get_ResourceType](./get_resourcetype/)() const | Typ der Ressource. |
| [get_Uri](./get_uri/)() const | URI der Ressource, die zum Herunterladen verwendet wird, wenn [ResourceLoading()](../iresourceloadingcallback/resourceloading/) [Default](../resourceloadingaction/) zurückgibt. Anfangs ist sie auf die absolute URI der Ressource gesetzt, aber der Benutzer kann sie auf einen beliebigen Wert neu definieren. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Setter für [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Setzt vom Benutzer bereitgestellte Daten der Ressource, die verwendet werden, wenn [ResourceLoading()](../iresourceloadingcallback/resourceloading/) [UserProvided](../resourceloadingaction/) zurückgibt. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
