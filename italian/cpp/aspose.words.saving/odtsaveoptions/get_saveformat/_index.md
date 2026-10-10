---
title: "Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat method"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat method. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere Odt o Ott in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/odtsaveoptions/get_saveformat/
---
## OdtSaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere [Odt](../../../aspose.words/saveformat/) o [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
