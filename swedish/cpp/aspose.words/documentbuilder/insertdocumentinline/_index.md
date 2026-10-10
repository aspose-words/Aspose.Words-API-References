---
title: "Aspose::Words::DocumentBuilder::InsertDocumentInline metod"
linktitle: "InsertDocumentInline"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertDocumentInline metod. Infogar ett dokument inline vid markörens position i C++."
type: docs
weight: 33500
url: /sv/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Infogar ett dokument inline på markörens position.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Källdokument för infogning. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Tillåter att ange alternativ som påverkar formateringen av ett resultatsdokument. |

### ReturnValue

Första noden i det infogade innehållet.
## Anmärkningar


Denna metod efterliknar MS Word‑beteendet, som om CTRL+'A' (markera allt innehåll) trycktes, sedan CTRL+'C' (kopiera markerat till bufferten) i ett dokument och sedan CTRL+'V' (infoga innehåll från bufferten) i ett annat dokument.

Till skillnad från [InsertDocument()](../) flyttar den här metoden innehållet i stycket i destinationsdokumentet, före vilket källdokumentet infogas, till det sista stycket i det infogade källdokumentet. Detta innebär faktiskt att styckeavbrottet för det sista infogade stycket tas bort.

Obs, om den sista noden i källdokumentet inte är ett stycke, görs ingenting.

## Exempel



Visar hur man infogar ett dokument inline vid markörens position.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Skapa destinationsdokument.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Infoga källdokumentet i destinationen inline.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## Se även

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
