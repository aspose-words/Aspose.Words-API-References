---
title: "Aspose::Words::Saving::DocSaveOptions::get_Password metodo"
linktitle: "get_Password"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_Password metodo. Ottiene/imposta una password per crittografare il documento usando il metodo di crittografia RC4 in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


Ottiene/imposta una password per crittografare il documento usando il metodo di crittografia RC4.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## Note


Per salvare il documento senza crittografia, questa proprietà dovrebbe essere **null** o una stringa vuota.

## Esempi



Mostra come impostare le opzioni di salvataggio per i formati Microsoft Word più vecchi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Imposta una password che proteggerà il caricamento del documento da parte di Microsoft Word o Aspose.Words.
// Nota che ciò non crittografa in alcun modo il contenuto del documento.
options->set_Password(u"MyPassword");

// Se il documento contiene una busta di instradamento, possiamo preservarla durante il salvataggio impostando questo flag su true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// Per poter caricare il documento,
// dovremo applicare la password che abbiamo specificato nell'oggetto DocSaveOptions in un oggetto LoadOptions.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
