---
title: Class PlainTextDocument
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.PlainTextDocument klas. Ermöglicht das Extrahieren einer Klartextdarstellung des Inhalts des Dokuments.
type: docs
weight: 4190
url: /de/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Ermöglicht das Extrahieren einer Klartextdarstellung des Inhalts des Dokuments.

```csharp
public class PlainTextDocument
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(Stream) | Erstellt ein Nur-Text-Dokument aus einem Stream. Erkennt automatisch das Dateiformat. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(string) | Erstellt aus einer Datei ein Nur-Text-Dokument. Erkennt automatisch das Dateiformat. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(Stream, LoadOptions) | Erstellt ein Nur-Text-Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(string, LoadOptions) | Erstellt aus einer Datei ein Nur-Text-Dokument. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | erhält[`BuiltInDocumentProperties`](./builtindocumentproperties/) des Dokuments. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | erhält[`CustomDocumentProperties`](./customdocumentproperties/) des Dokuments. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Ruft den Textinhalt des Dokuments als Zeichenfolge verkettet ab. |

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


