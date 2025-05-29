---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words für .NET
description: Konvertieren Sie Ihre ParagraphCollection mühelos mit der ToArray-Methode in ein Array, optimieren Sie so die Datenverwaltung und verbessern Sie Ihre Dokumentverarbeitung.
type: docs
weight: 20
url: /de/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Kopiert alle Absätze aus der Sammlung in ein neues Absatz-Array.

```csharp
public Paragraph[] ToArray()
```

### Rückgabewert

Ein Array von Absätzen.

## Beispiele

Zeigt, wie ein Array aus einer NodeCollection erstellt wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Zeigt, wie man mit „Hot Remove“ einen Knoten während der Enumeration entfernt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Entfernen Sie mitten in einer Aufzählung einen Knoten aus der Sammlung.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
