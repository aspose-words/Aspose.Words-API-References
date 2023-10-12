---
title: Class PlainTextDocument
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.PlainTextDocument klas. Ermöglicht das Extrahieren einer Klartextdarstellung des Dokumentinhalts.
type: docs
weight: 4440
url: /de/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Ermöglicht das Extrahieren einer Klartextdarstellung des Dokumentinhalts.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Textdokumenten](https://docs.aspose.com/words/net/working-with-text-document/) Dokumentationsartikel.

```csharp
public class PlainTextDocument
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(Stream) | Erstellt ein Nur-Text-Dokument aus einem Stream. Erkennt automatisch das Dateiformat. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(string) | Erstellt ein Nur-Text-Dokument aus einer Datei. Erkennt automatisch das Dateiformat. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(Stream, LoadOptions) | Erstellt ein Nur-Text-Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(string, LoadOptions) | Erstellt ein Nur-Text-Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Ruft ab[`BuiltInDocumentProperties`](./builtindocumentproperties/) des Dokuments. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Ruft ab[`CustomDocumentProperties`](./customdocumentproperties/) des Dokuments. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Ruft den als String verketteten Textinhalt des Dokuments ab. |

### Beispiele

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


