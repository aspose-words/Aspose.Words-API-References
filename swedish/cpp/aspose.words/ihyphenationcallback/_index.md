---
title: "Aspose::Words::IHyphenationCallback interface"
linktitle: "IHyphenationCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IHyphenationCallback‑gränssnitt. Implementeras av klasser som kan registrera avstavningsordböcker i C++."
type: docs
weight: 78000
url: /sv/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Implementeras av klasser som kan registrera avstavnings-ordlistor.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Meddelar applikationen att avstavningsordboken för det angivna språket inte hittades och kan behöva registreras. Implementeringen bör hitta en ordbok och registrera den med hjälp av [RegisterDictionary()](../)-metoderna. Om ordboken inte är tillgänglig för det angivna språket kan implementeringen avstå från ytterligare anrop för samma språk genom att använda [RegisterDictionary()](../) med **null**‑värde. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
