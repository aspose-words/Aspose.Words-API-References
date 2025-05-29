---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words für .NET
description: Entdecken Sie die ListIndentation-Eigenschaft von TxtSaveOptions, die die Listeneinrückung für eine bessere Lesbarkeit anpasst. Steuern Sie Zeichen und Ebenen mühelos!
type: docs
weight: 30
url: /de/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Erhält eine[`TxtListIndentation`](../../txtlistindentation/)Objekt, das angibt, wie viele und welche Zeichen zum Einrücken der Listenebenen verwendet werden sollen. Standardmäßig ist die Anzahl der Zeichen „\0“ gleich null, d. h. es wird keine Einrückung vorgenommen.

```csharp
public TxtListIndentation ListIndentation { get; }
```

## Beispiele

Zeigt, wie die Listeneinrückung beim Speichern eines Dokuments im Klartext konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Liste mit drei Einrückungsebenen.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Legen Sie die Eigenschaft "Character" fest, um ein zu verwendendes Zeichen zuzuweisen
// zum Auffüllen, das Listeneinrückungen im Klartext simuliert.
txtSaveOptions.ListIndentation.Character = ' ';

// Legen Sie die Eigenschaft „Count“ fest, um die Anzahl der
// um das Füllzeichen für jede Listeneinzugsebene zu platzieren.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Siehe auch

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
