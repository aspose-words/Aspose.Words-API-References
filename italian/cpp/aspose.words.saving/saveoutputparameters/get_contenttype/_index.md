---
title: "Metodo Aspose::Words::Saving::SaveOutputParameters::get_ContentType"
linktitle: "get_ContentType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SaveOutputParameters::get_ContentType. Restituisce la stringa Content-Type (Internet Media Type) che identifica il tipo del documento salvato in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Restituisce la stringa Content-Type (Internet Media Type) che identifica il tipo del documento salvato.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Esempi



Mostra come accedere ai parametri di output dell'operazione di salvataggio di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Dopo aver salvato un documento, possiamo accedere all'Internet Media Type (tipo MIME) del nuovo documento di output creato.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Questa proprietà cambia a seconda del formato di salvataggio.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Vedi anche

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
