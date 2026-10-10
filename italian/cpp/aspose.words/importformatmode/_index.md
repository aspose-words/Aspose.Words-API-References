---
title: "Aspose::Words::ImportFormatMode enum"
linktitle: "ImportFormatMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatMode enum. Specifica come la formattazione viene unita durante l'importazione di contenuti da un altro documento in C++."
type: docs
weight: 93000
url: /it/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Specifica come la formattazione viene unita durante l'importazione di contenuti da un altro documento.

```cpp
enum class ImportFormatMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseDestinationStyles | 0 | Utilizza gli stili del documento di destinazione e copia i nuovi stili. Questa è l'opzione predefinita. |
| KeepSourceFormatting | 1 | Copia tutti gli stili necessari nel documento di destinazione, genera nomi di stile unici se necessario. |
| KeepDifferentStyles | 2 | Copia solo gli stili che sono diversi da quelli nel documento di origine. |

## Note


Quando copi i nodi da un documento a un altro, questa opzione specifica come viene risolto il formato quando entrambi i documenti hanno uno stile con lo stesso nome, ma formattazione diversa.

La formattazione viene risolta come segue:

1. Gli stili incorporati vengono abbinati usando il loro identificatore di stile indipendente dalla locale. Gli stili definiti dall'utente vengono abbinati usando il nome dello stile sensibile al maiuscolo/minuscolo.
1. Se non viene trovato uno stile corrispondente nel documento di destinazione, lo stile (e tutti gli stili a cui fa riferimento) vengono copiati nel documento di destinazione e i nodi importati vengono aggiornati per fare riferimento al nuovo stile.
1. Se uno stile corrispondente esiste già nel documento di destinazione, ciò che accade dipende dal parametro **importFormatMode** passato a [ImportNode()](../) come descritto di seguito.



Quando si utilizza l'opzione [UseDestinationStyles](./), se uno stile corrispondente esiste già nel documento di destinazione, lo stile non viene copiato e i nodi importati vengono aggiornati per fare riferimento allo stile esistente.

Lo svantaggio dell'utilizzo di [UseDestinationStyles](./) è che il testo importato potrebbe apparire diverso nel documento di destinazione rispetto al documento di origine. Per esempio, lo stile "Heading 1" nel documento di origine utilizza il carattere Arial 16pt e lo stile "Heading 1" nel documento di destinazione utilizza il carattere Times New Roman 14pt. Quando si importa il testo con lo stile "Heading 1" senza altra formattazione diretta, apparirà come Times New Roman 14pt nel documento di destinazione.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

Lo svantaggio dell'utilizzo di [KeepSourceFormatting](./) è che, se si eseguono diversi import, si potrebbero accumulare molti stili nel documento di destinazione e ciò potrebbe rendere difficile utilizzare una formattazione di stile coerente in Microsoft Word per questo documento.

L'utilizzo dell'opzione [KeepDifferentStyles](./) consente di riutilizzare gli stili di destinazione se la formattazione che forniscono è identica a quella degli stili nel documento di origine. Se lo stile nel documento di destinazione è diverso da quello di origine, allora viene importato.

## Esempi



Mostra come inserire un documento in un altro documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
