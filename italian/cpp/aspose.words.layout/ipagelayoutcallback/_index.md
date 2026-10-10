---
title: "Aspose::Words::Layout::IPageLayoutCallback interfaccia"
linktitle: "IPageLayoutCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::IPageLayoutCallback interfaccia. Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante la costruzione e il rendering del modello di layout di pagina in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante la costruzione e il rendering del modello di layout di pagina.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Questo viene chiamato per notificare l'avanzamento della costruzione e del rendering del layout. |
| static [Type](./type/)() |  |
## Note


L'uso principale di questa interfaccia è consentire al codice dell'applicazione di interrompere il processo di costruzione.

È possibile costruire il modello di layout di pagina per solo alcune pagine all'inizio del documento, quindi interrompere il processo e renderizzare solo ciò che è già stato costruito.

Nota, tuttavia, che i risultati del rendering potrebbero non corrispondere a quanto sarebbe stato renderizzato per ogni pagina se il processo fosse terminato.

Questa tecnica potrebbe non funzionare per tutti i documenti o potrebbe fallire completamente.

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
