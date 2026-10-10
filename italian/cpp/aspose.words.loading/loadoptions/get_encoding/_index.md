---
title: "Aspose::Words::Loading::LoadOptions::get_Encoding metodo"
linktitle: "get_Encoding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_Encoding metodo. Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere null. Il valore predefinito è null in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere **null**. Il valore predefinito è **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Note


Questa proprietà è utilizzata solo durante il caricamento di documenti HTML, TXT o CHM.

Se la codifica non è specificata all'interno del documento e questa proprietà è **null**, il sistema proverà a rilevare automaticamente la codifica.

## Esempi



Mostra come impostare la codifica con cui aprire un documento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Carica il documento passando l'oggetto LoadOptions, quindi verifica il contenuto del documento.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
