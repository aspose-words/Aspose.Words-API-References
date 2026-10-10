---
title: "Aspose::Words::PlainTextDocument Klasse"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PlainTextDocument Klasse. Ermöglicht das Extrahieren einer Nur-Text-Darstellung des Inhalts des Dokuments. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 50000
url: /de/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Ermöglicht das Extrahieren einer Nur‑Text‑Darstellung des Inhalts des Dokuments. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Ruft die [BuiltInDocumentProperties](./get_builtindocumentproperties/) des Dokuments ab. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Ruft die [CustomDocumentProperties](./get_customdocumentproperties/) des Dokuments ab. |
| [get_Text](./get_text/)() const | Ruft den Textinhalt des Dokuments ab, zusammengefügt als Zeichenkette. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Erstellt ein Nur-Text-Dokument aus einer Datei. Erkennt das Dateiformat automatisch. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Erstellt ein Nur-Text-Dokument aus einer Datei. Ermöglicht das Angeben zusätzlicher Optionen wie ein Verschlüsselungspasswort. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Erstellt ein Nur-Text-Dokument aus einem Stream. Erkennt das Dateiformat automatisch. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Erstellt ein Nur-Text-Dokument aus einem Stream. Ermöglicht das Angeben zusätzlicher Optionen wie ein Verschlüsselungspasswort. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
