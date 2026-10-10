---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password metodo"
linktitle: "get_Password"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password metodo. Ottiene/imposta una password per crittografare il documento utilizzando l'algoritmo di crittografia standard ECMA376 in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Ottiene/imposta una password per crittografare il documento usando l'algoritmo di crittografia ECMA376 Standard.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Note


Per salvare il documento senza crittografia, questa proprietà dovrebbe essere **null** o una stringa vuota.

## Esempi



Mostra come creare un documento Office Open XML crittografato con password.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// Non saremo in grado di aprire questo documento con Microsoft Word o
// Aspose.Words senza fornire la password corretta.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Apri il documento crittografato passando la password corretta in un oggetto LoadOptions.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
