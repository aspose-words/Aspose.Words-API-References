---
title: "Aspose::Words::IHyphenationCallback::RequestDictionary metod"
linktitle: "RequestDictionary"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IHyphenationCallback::RequestDictionary metod. Meddelar applikationen att avstavningsordbok för det angivna språket inte hittades och kan behöva registreras. Implementeringen bör hitta en ordbok och registrera den med RegisterDictionary() metoder. Om ordboken inte är tillgänglig för det angivna språket kan implementeringen välja att avbryta ytterligare anrop för samma språk genom att använda RegisterDictionary() med nullvärde i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Meddelar applikationen att avstavningsordboken för det angivna språket inte hittades och kan behöva registreras. Implementeringen bör hitta en ordbok och registrera den med hjälp av [RegisterDictionary()](../)-metoderna. Om ordboken inte är tillgänglig för det angivna språket kan implementeringen avstå från ytterligare anrop för samma språk genom att använda [RegisterDictionary()](../) med **null**‑värde.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| språk | System::String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "culture name" och RFC 4646 för detaljer. |

## Se även

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
