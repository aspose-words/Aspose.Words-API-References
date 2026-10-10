---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties méthode"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties méthode. Obtient les BuiltInDocumentProperties du document en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Obtient [BuiltInDocumentProperties](./) du document.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Exemples



Montre comment charger le contenu d'un document Microsoft Word en texte brut, puis accéder aux propriétés intégrées du document original.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASSERT_EQ(u"John Doe", plaintext->get_BuiltInDocumentProperties()->get_Author());
```

## Voir aussi

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
