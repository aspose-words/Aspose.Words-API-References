---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words für .NET
description: Entdecken Sie die SharedDocument-Funktion „BuiltInDocumentProperties“, die anzeigt, ob Ihr Dokument freigegeben ist, und so die Zusammenarbeit und Zugänglichkeit verbessert.
type: docs
weight: 280
url: /de/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

Gibt an, ob es sich bei dem Dokument um ein freigegebenes Dokument handelt.

```csharp
public bool SharedDocument { get; }
```

## Bemerkungen

Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele

Zeigt, wie erweiterte Eigenschaften abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
