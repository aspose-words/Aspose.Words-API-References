---
title: "Aspose::Words::Saving::IFontSavingCallback interfaccia"
linktitle: "IFontSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::IFontSavingCallback interfaccia. Implementa questa interfaccia se desideri ricevere notifiche e controllare come Aspose.Words salva i caratteri durante l'esportazione di un documento in formato HTML in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Implementa questa interfaccia se desideri ricevere notifiche e controllare come Aspose.Words salva i font durante l'esportazione di un documento nel formato HTML.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Chiamata quando Aspose.Words sta per salvare una risorsa di carattere. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
