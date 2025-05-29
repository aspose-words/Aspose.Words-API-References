---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Methode „UnlinkFields“ effizient die Verknüpfung von Feldern in Ihrem gesamten Dokument aufheben und so Ihren Bearbeitungs-Workflow verbessern können.
type: docs
weight: 780
url: /de/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Hebt die Verknüpfung von Feldern im gesamten Dokument auf.

```csharp
public void UnlinkFields()
```

## Bemerkungen

Ersetzt alle Felder im gesamten Dokument durch ihre aktuellsten Ergebnisse.

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
