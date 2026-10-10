---
title: "Metodo Aspose::Words::IHyphenationCallback::RequestDictionary. Notifica all'applicazione che il dizionario di sillabazione per la lingua specificata non è stato trovato e potrebbe dover essere registrato. L'implementazione dovrebbe trovare un dizionario e registrarlo usando i metodi RegisterDictionary(). Se il dizionario non è disponibile per la lingua specificata, l'implementazione può rinunciare a ulteriori chiamate per la stessa lingua usando RegisterDictionary() con valore null in C++."
linktitle: "Metodo Aspose::Words::IHyphenationCallback::GetType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Come utilizzare il metodo GetType della classe Aspose::Words::IHyphenationCallback in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Notifica all'applicazione che il dizionario di sillabazione per la lingua specificata non è stato trovato e potrebbe dover essere registrato. L'implementazione dovrebbe trovare un dizionario e registrarlo utilizzando i metodi [RegisterDictionary()](../). Se il dizionario non è disponibile per la lingua specificata, l'implementazione può rinunciare a ulteriori chiamate per la stessa lingua utilizzando [RegisterDictionary()](../) con valore **null**.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lingua | System::String | Un nome di lingua, ad es. "en-US". Vedere la documentazione .NET per "culture name" e RFC 4646 per i dettagli. |

## Vedi anche

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
