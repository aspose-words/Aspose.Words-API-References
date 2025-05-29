---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.PlainTextDocument, um mühelos Klartext aus Ihren Dokumenten zu extrahieren und zu verwenden, um die Lesbarkeit und Verarbeitung zu verbessern.
type: docs
weight: 5170
url: /de/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Ermöglicht das Extrahieren der Klartextdarstellung des Dokumentinhalts.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Textdokumenten](https://docs.aspose.com/words/net/working-with-text-document/) Dokumentationsartikel.

```csharp
public class PlainTextDocument
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Erstellt ein reines Textdokument aus einem Stream. Das Dateiformat wird automatisch erkannt. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Erstellt ein reines Textdokument aus einer Datei. Das Dateiformat wird automatisch erkannt. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Erstellt ein reines Textdokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Erstellt ein reines Textdokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Ruft ab[`BuiltInDocumentProperties`](./builtindocumentproperties/) des Dokuments. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Ruft ab[`CustomDocumentProperties`](./customdocumentproperties/) des Dokuments. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Ruft den Textinhalt des Dokuments als Zeichenfolge ab. |

## Beispiele

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen wird.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
