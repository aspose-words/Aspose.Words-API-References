---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words für .NET
description: Document UnlinkFields methode. Hebt die Verknüpfung von Feldern im gesamten Dokument auf in C#.
type: docs
weight: 730
url: /de/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Hebt die Verknüpfung von Feldern im gesamten Dokument auf.

```csharp
public void UnlinkFields()
```

## Bemerkungen

Ersetzt alle Felder im gesamten Dokument durch ihre neuesten Ergebnisse.

Um die Verknüpfung von Feldern in einem bestimmten Teil des Dokuments aufzuheben, verwenden Sie[`UnlinkFields`](../../range/unlinkfields/).

## Beispiele

Zeigt, wie die Verknüpfung aller Felder im Dokument aufgehoben wird.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
