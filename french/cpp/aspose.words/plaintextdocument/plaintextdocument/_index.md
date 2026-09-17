---
title: "Constructeur Aspose::Words::PlainTextDocument::PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::PlainTextDocument::PlainTextDocument. Crée un document texte brut à partir d'un flux. Détecte automatiquement le format du fichier en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Crée un document texte brut à partir d'un flux. Détecte automatiquement le format du fichier.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux à partir duquel extraire le texte. |
## Remarques


Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

## Exemples



Montre comment charger le contenu d'un document Microsoft Word en texte brut à l'aide d'un flux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## Voir aussi

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Crée un document texte brut à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux à partir duquel extraire le texte. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Options supplémentaires à utiliser lors du chargement d'un document. Peut être **null**. |
## Remarques


Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

## Exemples



Montre comment charger le contenu d'un document Microsoft Word chiffré en texte brut à l'aide d'un flux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream, loadOptions);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&) constructor


Crée un document texte brut à partir d'un fichier. Détecte automatiquement le format du fichier.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom du fichier à partir duquel extraire le texte. |

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
## PlainTextDocument::PlainTextDocument(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Crée un document texte brut à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom du fichier à partir duquel extraire le texte. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Options supplémentaires à utiliser lors du chargement d'un document. Peut être **null**. |

## Exemples



Montre comment charger le contenu d'un document Microsoft Word chiffré en texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", loadOptions);

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream)
```

## Voir aussi

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
