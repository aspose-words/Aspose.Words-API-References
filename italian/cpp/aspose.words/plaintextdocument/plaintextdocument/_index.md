---
title: "Costruttore Aspose::Words::PlainTextDocument::PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::PlainTextDocument::PlainTextDocument. Crea un documento di testo semplice da uno stream. Rileva automaticamente il formato del file in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Crea un documento di testo semplice da uno stream. Rileva automaticamente il formato del file.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream da cui estrarre il testo. |
## Note


Il documento deve essere posizionato all'inizio dello stream. Lo stream deve supportare il posizionamento casuale.

## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word in testo semplice utilizzando uno stream.
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

## Vedi anche

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Crea un documento di testo semplice da uno stream. Consente di specificare opzioni aggiuntive come una password di crittografia.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream da cui estrarre il testo. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Può essere **null**. |
## Note


Il documento deve essere posizionato all'inizio dello stream. Lo stream deve supportare il posizionamento casuale.

## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word crittografato in testo semplice utilizzando uno stream.
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

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&) constructor


Crea un documento di testo semplice da un file. Rileva automaticamente il formato del file.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome del file da cui estrarre il testo. |

## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Vedi anche

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Crea un documento di testo semplice da un file. Consente di specificare opzioni aggiuntive come una password di crittografia.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome del file da cui estrarre il testo. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Può essere **null**. |

## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word crittografato in testo semplice.
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

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream)
```

## Vedi anche

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
