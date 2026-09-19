---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password metodo"
linktitle: "get_Password"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password metodo. Ottiene o imposta una password per cifrare il documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


Ottiene o imposta una password per crittografare il documento.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## Note


Per salvare il documento senza crittografia, questa proprietà dovrebbe essere **null** o una stringa vuota.

## Esempi



Mostra come crittografare un documento ODT/OTT salvato con una password, e poi caricarlo usando Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Crea un nuovo OdtSaveOptions, e passa "SaveFormat.Odt",
// o "SaveFormat.Ott" come formato per salvare il documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Se apriamo questo documento con un editor appropriato,
// ti chiederà la password che abbiamo specificato nell'oggetto SaveOptions.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Se desideriamo aprire o modificare nuovamente questo documento usando Aspose.Words,
// dovremo fornire un oggetto LoadOptions con la password corretta al costruttore di caricamento.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
