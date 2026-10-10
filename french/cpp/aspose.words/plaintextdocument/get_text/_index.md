---
title: "Méthode Aspose::Words::PlainTextDocument::get_Text"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PlainTextDocument::get_Text. Obtient le contenu textuel du document concaténé sous forme de chaîne en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Obtient le contenu textuel du document concaténé sous forme de chaîne.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## Exemples



Montre comment charger le contenu d'un document Microsoft Word en texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Voir aussi

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
