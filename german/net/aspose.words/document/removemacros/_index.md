---
title: Document.RemoveMacros
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Entfernt alle Makros das VBAProjekt sowie Symbolleisten und Befehlsanpassungen aus dem Dokument.
type: docs
weight: 690
url: /de/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Entfernt alle Makros (das VBA-Projekt) sowie Symbolleisten und Befehlsanpassungen aus dem Dokument.

```csharp
public void RemoveMacros()
```

### Bemerkungen

Durch das Entfernen aller Makros aus einem Dokument können Sie sicherstellen, dass das Dokument keine Makroviren enthält.

### Beispiele

Zeigt, wie alle Makros aus einem Dokument entfernt werden.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Entfernen Sie das VBA-Projekt des Dokuments zusammen mit allen seinen Makros.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


