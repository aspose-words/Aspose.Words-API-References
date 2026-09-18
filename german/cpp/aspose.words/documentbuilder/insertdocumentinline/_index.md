---
title: "Aspose::Words::DocumentBuilder::InsertDocumentInline Methode"
linktitle: "InsertDocumentInline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertDocumentInline Methode. Fügt ein Dokument inline an der Cursorposition in C++ ein."
type: docs
weight: 33500
url: /de/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Fügt ein Dokument inline an der Cursor‑Position ein.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Quelldokument zum Einfügen. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Ermöglicht das Festlegen von Optionen, die die Formatierung eines Ergebnisdokuments beeinflussen. |

### ReturnValue

Erster Knoten des eingefügten Inhalts.
## Hinweise


Diese Methode ahmt das Verhalten von MS Word nach, als ob CTRL+'A' (alles auswählen) gedrückt würde, dann CTRL+'C' (ausgewählte Inhalte in den Zwischenspeicher kopieren) in einem Dokument und anschließend CTRL+'V' (Inhalte aus dem Zwischenspeicher einfügen) in einem anderen Dokument.

Im Unterschied zu [InsertDocument()](../) verschiebt diese Methode den Inhalt des Absatzes des Zieldokuments, vor dem das Quelldokument eingefügt wird, in den letzten Absatz des eingefügten Quelldokuments. Das bedeutet tatsächlich, dass der Absatzumbruch des zuletzt eingefügten Absatzes entfernt wird.

Hinweis: Wenn der letzte Knoten des Quelldokuments kein Absatz ist, wird nichts unternommen.

## Beispiele



Zeigt, wie man ein Dokument inline an der Cursorposition einfügt.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Erstelle Zieldokument.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Füge das Quelldokument inline in das Ziel ein.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## Siehe auch

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
