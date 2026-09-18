---
title: "Aspose::Words::PlainTextDocument::get_Text‑Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PlainTextDocument::get_Text‑Methode. Gibt den Textinhalt des Dokuments als verketteten String in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Ruft den Textinhalt des Dokuments ab, zusammengefügt als Zeichenkette.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


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
