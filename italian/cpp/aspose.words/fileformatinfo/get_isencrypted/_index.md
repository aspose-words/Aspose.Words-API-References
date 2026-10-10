---
title: "Metodo Aspose::Words::FileFormatInfo::get_IsEncrypted"
linktitle: "get_IsEncrypted"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::FileFormatInfo::get_IsEncrypted. Restituisce true se il documento è crittografato e richiede una password per aprirlo in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Restituisce **true** se il documento è crittografato e richiede una password per l'apertura.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Note


Questa proprietà esiste per aiutarti a distinguere i documenti crittografati da quelli non crittografati. Se tenti di caricare un documento crittografato usando Aspose.Words senza fornire una password, verrà generata un'eccezione. Puoi utilizzare questa proprietà per rilevare se un documento richiede una password e intraprendere un'azione prima di caricare il documento, ad esempio chiedere all'utente di inserire una password.

## Esempi



Mostra come utilizzare la classe [FileFormatUtil](../../fileformatutil/) per rilevare il formato del documento e la crittografia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configura un oggetto SaveOptions per crittografare il documento
// con una password quando lo salviamo, e poi salva il documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verifica il tipo di file del nostro documento e il suo stato di crittografia.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## Vedi anche

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
