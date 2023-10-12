---
title: Document.UnlinkFields
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Hebt die Verknüpfung von Feldern im gesamten Dokument auf.
type: docs
weight: 750
url: /de/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Hebt die Verknüpfung von Feldern im gesamten Dokument auf.

```csharp
public void UnlinkFields()
```

### Bemerkungen

Ersetzt alle Felder im gesamten Dokument durch ihre neuesten Ergebnisse.

Um die Verknüpfung von Feldern in einem bestimmten Teil des Dokuments aufzuheben, verwenden Sie[`UnlinkFields`](../../range/unlinkfields/).

### Beispiele

Zeigt, wie die Verknüpfung aller Felder im Dokument aufgehoben wird.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


