---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der Methode „RemoveBlankPages“ und entfernen Sie unerwünschte leere Seiten für ein elegantes, professionelles Finish.
type: docs
weight: 700
url: /de/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Entfernt leere Seiten aus dem Dokument.

```csharp
public List<int> RemoveBlankPages()
```

### Rückgabewert

Die Liste der Seitenzahlen wurde als leer betrachtet und entfernt.

## Bemerkungen

Das resultierende Dokument enthält keine Seiten, die als leer betrachtet werden, während andere Inhalte, einschließlich Nummerierung, Kopf-/Fußzeilen und Gesamtlayout unverändert bleiben sollten. Eine Seite gilt als leer, wenn der Hauptteil der Seite keinen sichtbaren Inhalt hat, z. B. eine leere Tabelle ohne Rahmen wird als unsichtbar betrachtet und daher wird die Seite als leer erkannt.

## Beispiele

Zeigt, wie leere Seiten aus dem Dokument entfernt werden.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
