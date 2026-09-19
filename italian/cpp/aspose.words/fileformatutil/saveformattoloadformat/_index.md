---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat metodo"
linktitle: "SaveFormatToLoadFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat metodo. Converte un valore SaveFormat in un valore LoadFormat, se possibile, in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Converte un valore [SaveFormat](../../saveformat/) in un valore [LoadFormat](../../loadformat/) se possibile.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Esempi



Mostra come convertire un formato di salvataggio nel corrispondente formato di caricamento.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Alcuni tipi di file possono avere documenti salvati, ma non caricati, utilizzando Aspose.Words.
// Se proviamo a convertire un formato di salvataggio di questo tipo in un formato di caricamento, verrà generata un'eccezione.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## Vedi anche

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
