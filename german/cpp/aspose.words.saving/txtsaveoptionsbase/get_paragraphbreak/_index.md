---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak Methode"
linktitle: "get_ParagraphBreak"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak Methode. Gibt die Zeichenfolge an, die als Absatzumbruch beim Export in Textformate in C++ verwendet wird."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Gibt die Zeichenkette an, die als Absatztrennung beim Export in Textformate verwendet wird.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Hinweise


Der Standardwert ist [CrLf](../../../aspose.words/controlchar/crlf/).

## Beispiele



Zeigt, wie man ein .txt-Dokument mit einem benutzerdefinierten Absatzumbruch speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument in Klartext speichern.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Setze die "ParagraphBreak"-Eigenschaft auf einen benutzerdefinierten Wert, den wir am Ende jedes Absatzes einfügen möchten.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Siehe auch

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
