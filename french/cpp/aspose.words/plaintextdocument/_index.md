---
title: "Aspose::Words::PlainTextDocument classe"
linktitle: "PlainTextDocument"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PlainTextDocument classe. Permet d'extraire la représentation en texte brut du contenu du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 50000
url: /fr/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Permet d'extraire la représentation en texte brut du contenu du document. Pour en savoir plus, consultez l'article de documentation [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Obtient les [BuiltInDocumentProperties](./get_builtindocumentproperties/) du document. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Obtient les [CustomDocumentProperties](./get_customdocumentproperties/) du document. |
| [get_Text](./get_text/)() const | Obtient le contenu textuel du document concaténé sous forme de chaîne. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Crée un document texte brut à partir d'un fichier. Détecte automatiquement le format du fichier. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Crée un document texte brut à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Crée un document texte brut à partir d'un flux. Détecte automatiquement le format du fichier. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Crée un document texte brut à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
