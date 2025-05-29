---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Duplizieren Sie Abschnitte mühelos mit unserer Abschnittsklon-Methode. Optimieren Sie Ihren Workflow und steigern Sie Ihre Produktivität mit diesem leistungsstarken Tool!
type: docs
weight: 130
url: /de/net/aspose.words/section/clone/
---
## Section.Clone method

Erstellt ein Duplikat dieses Abschnitts.

```csharp
public Section Clone()
```

## Beispiele

Zeigt, wie Abschnitte in einem Dokument hinzugefügt und entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Löschen Sie den ersten Abschnitt aus dem Dokument.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Fügen Sie eine Kopie des jetzigen ersten Abschnitts an das Ende des Dokuments an.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
