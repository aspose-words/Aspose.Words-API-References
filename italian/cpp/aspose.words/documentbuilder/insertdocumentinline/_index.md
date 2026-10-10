---
title: "Metodo Aspose::Words::DocumentBuilder::InsertDocumentInline"
linktitle: "InsertDocumentInline"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertDocumentInline. Inserisce un documento in linea nella posizione del cursore in C++."
type: docs
weight: 33500
url: /it/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Inserisce un documento in linea nella posizione del cursore.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Documento sorgente da inserire. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Consente di specificare opzioni che influenzano la formattazione di un documento risultato. |

### ReturnValue

Primo nodo del contenuto inserito.
## Note


Questo metodo imita il comportamento di MS Word, come se si premessero CTRL+'A' (seleziona tutto il contenuto), poi CTRL+'C' (copia la selezione nel buffer) in un documento e poi CTRL+'V' (inserisce il contenuto dal buffer) in un altro documento.

Come differenza rispetto a [InsertDocument()](../) questo metodo sposta il contenuto del paragrafo del documento di destinazione, prima del quale viene inserito il documento sorgente, nell'ultimo paragrafo del documento sorgente inserito. In pratica, ciò significa che l'interruzione di paragrafo dell'ultimo paragrafo inserito viene rimossa.

Nota, se l'ultimo nodo del documento sorgente non è un paragrafo, non verrà eseguita alcuna operazione.

## Esempi



Mostra come inserire un documento in linea nella posizione del cursore.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Crea il documento di destinazione.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Inserisci il documento sorgente nel documento di destinazione in linea.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## Vedi anche

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
