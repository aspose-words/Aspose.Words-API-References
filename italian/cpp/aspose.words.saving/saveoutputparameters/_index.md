---
title: "Aspose::Words::Saving::SaveOutputParameters classe"
linktitle: "SaveOutputParameters"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SaveOutputParameters classe. Questo oggetto viene restituito al chiamante dopo che un documento è stato salvato e contiene informazioni aggiuntive che sono state generate o calcolate durante l'operazione di salvataggio. Il chiamante può utilizzare o ignorare questo oggetto. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Questo oggetto viene restituito al chiamante dopo che un documento è stato salvato e contiene informazioni aggiuntive generate o calcolate durante l'operazione di salvataggio. Il chiamante può utilizzare o ignorare questo oggetto. Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Restituisce la stringa Content-Type (Internet Media Type) che identifica il tipo del documento salvato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
