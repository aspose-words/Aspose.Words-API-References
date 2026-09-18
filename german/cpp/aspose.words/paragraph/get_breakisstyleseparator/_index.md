---
title: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator method"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator method. True, wenn dieser Absatzumbruch ein Style Separator ist. Ein Style Separator ermöglicht es einem Absatz, aus Teilen zu bestehen, die unterschiedliche Absatzformate haben, in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


True, wenn dieser Absatzumbruch ein [Style](../../style/) Separator ist. Ein Style Separator ermöglicht es einem Absatz, aus Teilen zu bestehen, die unterschiedliche Absatzformate haben.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Beispiele



Zeigt, wie man Text in dieselbe Zeile wie eine TOC‑Überschrift schreibt, ohne dass er im Inhaltsverzeichnis erscheint.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Fügen Sie einen Absatz mit einem Stil ein, den das Inhaltsverzeichnis als Eintrag erkennt.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Beide Zeichenketten befinden sich im selben Absatz und werden daher im selben Inhaltsverzeichnis‑Eintrag angezeigt.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Wenn wir einen Stil‑Trenner einfügen, können wir mehr Text im selben Absatz schreiben
// und einen anderen Stil verwenden, ohne im Inhaltsverzeichnis zu erscheinen.
// Wenn wir nach dem Trenner einen Überschrifts‑Stil verwenden, können wir mehrere Inhaltsverzeichnis‑Einträge aus einer Dokument‑Textzeile erzeugen.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## Siehe auch

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
