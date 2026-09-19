---
title: "Aspose::Words::IncorrectPasswordException typedef"
linktitle: "IncorrectPasswordException"
second_title: "Riferimento API Aspose.Words per C++"
description: "Typedef Aspose::Words::IncorrectPasswordException. Generato se un documento è crittografato con una password e la password specificata durante l'apertura del documento è errata o mancante. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 134000
url: /it/cpp/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException typedef


Generato se un documento è crittografato con una password e la password specificata durante l'apertura del documento è errata o mancante. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::IncorrectPasswordException = typedef System::ExceptionWrapper<Details_IncorrectPasswordException>
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
