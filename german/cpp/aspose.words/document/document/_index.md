---
title: "Aspose::Words::Document::Document Konstruktor"
linktitle: "Dokument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::Document Konstruktor. Erstellt ein leeres Word‑Dokument in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Erstellt ein leeres Word‑Dokument.

```cpp
Aspose::Words::Document::Document()
```

## Hinweise


Ein leeres Dokument wird aus den Ressourcen abgerufen und sieht standardmäßig eher aus, als wäre es von [Word2007](../../../aspose.words.settings/mswordversion/) erstellt worden. Dieses leere Dokument enthält eine Standardschriftartentabelle, minimale Standardsformatvorlagen und latente Formatvorlagen.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

Die Papiergröße des Dokuments ist standardmäßig Letter. Wenn Sie die Seiteneinrichtung ändern möchten, verwenden Sie [PageSetup](../../section/get_pagesetup/).

Nach der Erstellung können Sie [DocumentBuilder](../../documentbuilder/) verwenden, um Dokumentinhalte einfach hinzuzufügen.

## Beispiele



Zeigt, wie ein einfaches Dokument erstellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Neue Document‑Objekte enthalten standardmäßig den minimalen Satz von Knoten
// die erforderlich sind, um Inhalte wie Text und Formen hinzuzufügen: ein Section, ein Body und ein Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Zeigt, wie Dokumente erstellt und geladen werden.
```cpp
// Es gibt zwei Möglichkeiten, ein Document‑Objekt mit Aspose.Words zu erstellen.
// 1 -  Erstelle ein leeres Dokument:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Neue Document‑Objekte enthalten standardmäßig den minimalen Satz von Knoten
// die erforderlich sind, um Inhalte wie Text und Formen hinzuzufügen: ein Section, ein Body und ein Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Laden Sie ein Dokument, das im lokalen Dateisystem vorhanden ist:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Geladene Dokumente enthalten Inhalte, auf die wir zugreifen und die wir bearbeiten können.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Einige Vorgänge, die beim Laden ausgeführt werden müssen, wie das Verwenden eines Passworts zum Entschlüsseln eines Dokuments,
// können durch Übergeben eines LoadOptions-Objekts beim Laden des Dokuments durchgeführt werden.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Öffnet ein vorhandenes Dokument aus einem Stream. Erkennt das Dateiformat automatisch.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Stream, aus dem das Dokument geladen wird. |
## Hinweise


Das Dokument muss am Anfang des Streams gespeichert sein. Der Stream muss zufällige Positionierung unterstützen.

## Beispiele



Zeigt, wie ein Dokument mithilfe eines Streams geladen wird.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Öffnet ein vorhandenes Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie ein Verschlüsselungspasswort.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, aus dem das Dokument geladen wird. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Zusätzliche Optionen, die beim Laden eines Dokuments verwendet werden können. Kann **null** sein. |
## Hinweise


Das Dokument muss am Anfang des Streams gespeichert sein. Der Stream muss zufällige Positionierung unterstützen.

## Beispiele



Zeigt, wie man ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI öffnet.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Übergeben Sie beim Laden die URI des Basisordners
    // damit alle Bilder mit relativen URIs im HTML-Dokument gefunden werden können.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Überprüfen Sie, dass die erste Form des Dokuments ein gültiges Bild enthält.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```


Zeigt, wie man ein verschlüsseltes Microsoft Word-Dokument lädt.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words wirft eine Ausnahme, wenn wir versuchen, ein verschlüsseltes Dokument ohne dessen Passwort zu öffnen.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Beim Laden eines solchen Dokuments wird das Passwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 -  Laden Sie das Dokument vom lokalen Dateisystem über den Dateinamen:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Laden Sie das Dokument aus einem Stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Öffnet ein vorhandenes Dokument aus einer Datei. Erkennt das Dateiformat automatisch.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Dateiname des zu öffnenden Dokuments. |

## Beispiele



Zeigt, wie ein Dokument geöffnet und in .PDF konvertiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Öffnet ein vorhandenes Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie ein Verschlüsselungspasswort.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Dateiname des zu öffnenden Dokuments. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Zusätzliche Optionen, die beim Laden eines Dokuments verwendet werden können. Kann **null** sein. |

## Beispiele



Zeigt, wie Dokumente erstellt und geladen werden.
```cpp
// Es gibt zwei Möglichkeiten, ein Document‑Objekt mit Aspose.Words zu erstellen.
// 1 -  Erstelle ein leeres Dokument:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Neue Document‑Objekte enthalten standardmäßig den minimalen Satz von Knoten
// die erforderlich sind, um Inhalte wie Text und Formen hinzuzufügen: ein Section, ein Body und ein Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Laden Sie ein Dokument, das im lokalen Dateisystem vorhanden ist:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Geladene Dokumente enthalten Inhalte, auf die wir zugreifen und die wir bearbeiten können.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Einige Vorgänge, die beim Laden ausgeführt werden müssen, wie das Verwenden eines Passworts zum Entschlüsseln eines Dokuments,
// können durch Übergeben eines LoadOptions-Objekts beim Laden des Dokuments durchgeführt werden.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Zeigt, wie man ein verschlüsseltes Microsoft Word-Dokument lädt.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words wirft eine Ausnahme, wenn wir versuchen, ein verschlüsseltes Dokument ohne dessen Passwort zu öffnen.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Beim Laden eines solchen Dokuments wird das Passwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 -  Laden Sie das Dokument vom lokalen Dateisystem über den Dateinamen:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Laden Sie das Dokument aus einem Stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
