---
title: "Metodo Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding"
linktitle: "get_Encoding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding. Specifica la codifica da utilizzare durante l'esportazione in formati di testo. Il valore predefinito è Encoding.UTF8 in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/txtsaveoptionsbase/get_encoding/
---
## TxtSaveOptionsBase::get_Encoding method


Specifica la codifica da utilizzare durante l'esportazione in formati di testo. Il valore predefinito è **Encoding.UTF8**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding() const
```


## Esempi



Mostra come impostare la codifica per un documento di output .txt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi del testo con caratteri al di fuori del set di caratteri ASCII.
builder->Write(u"À È Ì Ò Ù.");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Verifica che la proprietà "Encoding" contenga la codifica appropriata per il contenuto del nostro documento.
ASPOSE_ASSERT_EQ(System::Text::Encoding::get_UTF8(), txtSaveOptions->get_Encoding());

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

System::String docText = System::Text::Encoding::get_UTF8()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt"));

ASSERT_EQ(u"\ufeffÀ È Ì Ò Ù.\r\n", docText);

// L'uso di una codifica non adatta può comportare la perdita del contenuto del documento.
txtSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());
doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System::Text::Encoding::get_ASCII()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt"));

ASSERT_EQ(u"? ? ? ? ?.\r\n", docText);
```

## Vedi anche

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
