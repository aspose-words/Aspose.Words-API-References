---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip method"
linktitle: "get_SaveRoutingSlip"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip method. Quando è false, i dati RoutingSlip non vengono salvati nel documento di output. Il valore predefinito è true in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.saving/docsaveoptions/get_saveroutingslip/
---
## DocSaveOptions::get_SaveRoutingSlip method


Quando **false**, i dati RoutingSlip non vengono salvati nel documento di output. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip() const
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

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
