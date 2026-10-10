---
title: "Aspose::Words::PlainTextDocument::PlainTextDocument-Konstruktor"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PlainTextDocument::PlainTextDocument-Konstruktor. Erstellt ein Nur-Text-Dokument aus einem Stream. Erkennt das Dateiformat automatisch in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Erstellt ein Nur-Text-Dokument aus einem Stream. Erkennt das Dateiformat automatisch.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, aus dem der Text extrahiert werden soll. |
## Hinweise


Das Dokument muss am Anfang des Streams gespeichert sein. Der Stream muss zufällige Positionierung unterstützen.

## Beispiele



Zeigt, wie man den Inhalt eines Microsoft Word-Dokuments im Nur-Text-Format mithilfe eines Streams lädt.
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

## Siehe auch

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Erstellt ein Nur-Text-Dokument aus einem Stream. Ermöglicht das Angeben zusätzlicher Optionen wie ein Verschlüsselungspasswort.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, aus dem der Text extrahiert werden soll. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Zusätzliche Optionen, die beim Laden eines Dokuments verwendet werden können. Kann **null** sein. |
## Hinweise


Das Dokument muss am Anfang des Streams gespeichert sein. Der Stream muss zufällige Positionierung unterstützen.

## Beispiele



Zeigt, wie man den Inhalt eines verschlüsselten Microsoft Word-Dokuments im Nur-Text-Format mithilfe eines Streams lädt.
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

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&) constructor


Erstellt ein Nur-Text-Dokument aus einer Datei. Erkennt das Dateiformat automatisch.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Name der Datei, aus der der Text extrahiert werden soll. |

## Beispiele



Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Nur-Text-Format geladen wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Siehe auch

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Erstellt ein Nur-Text-Dokument aus einer Datei. Ermöglicht das Angeben zusätzlicher Optionen wie ein Verschlüsselungspasswort.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Name der Datei, aus der der Text extrahiert werden soll. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Zusätzliche Optionen, die beim Laden eines Dokuments verwendet werden können. Kann **null** sein. |

## Beispiele



Zeigt, wie man den Inhalt eines verschlüsselten Microsoft‑Word‑Dokuments im Klartext lädt.
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

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream)
```

## Siehe auch

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
