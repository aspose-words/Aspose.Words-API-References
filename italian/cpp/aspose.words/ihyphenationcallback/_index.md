---
title: "Aspose::Words::IHyphenationCallback interface"
linktitle: "IHyphenationCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::IHyphenationCallback. Implementata da classi che possono registrare dizionari di sillabazione in C++."
type: docs
weight: 78000
url: /it/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Implementato da classi che possono registrare dizionari di sillabazione.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Notifica all'applicazione che il dizionario di sillabazione per la lingua specificata non è stato trovato e potrebbe dover essere registrato. L'implementazione dovrebbe trovare un dizionario e registrarlo utilizzando i metodi [RegisterDictionary()](../). Se il dizionario non è disponibile per la lingua specificata, l'implementazione può rinunciare a ulteriori chiamate per la stessa lingua utilizzando [RegisterDictionary()](../) con valore **null**. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
