---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: Aspose.Words für .NET
description: Document Cleanup methode. Bereinigt nicht verwendete Stile und Listen aus dem Dokument in C#.
type: docs
weight: 540
url: /de/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Bereinigt nicht verwendete Stile und Listen aus dem Dokument.

```csharp
public void Cleanup()
```

## Beispiele

Zeigt, wie nicht verwendete benutzerdefinierte Stile aus einem Dokument entfernt werden.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// In Kombination mit den integrierten Stilen verfügt das Dokument jetzt über acht Stile.
// Ein benutzerdefinierter Stil gilt als „verwendet“, wenn er auf einen Teil des Dokuments angewendet wird.
// was bedeutet, dass die vier von uns hinzugefügten Stile derzeit nicht verwendet werden.
Assert.AreEqual(8, doc.Styles.Count);

// Einen benutzerdefinierten Zeichenstil und dann einen benutzerdefinierten Listenstil anwenden. Dadurch werden die Stile als „gebraucht“ markiert.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// Durch das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wird, wird dieser erneut als „unbenutzt“ markiert.
// Führen Sie die Cleanup-Methode erneut aus, um sie zu entfernen.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Cleanup(*[CleanupOptions](../../cleanupoptions/)*) {#cleanup_1}

Bereinigt je nach Angabe nicht verwendete Stile und Listen aus dem Dokument[`CleanupOptions`](../../cleanupoptions/) .

```csharp
public void Cleanup(CleanupOptions options)
```

## Beispiele

Zeigt, wie alle nicht verwendeten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// In Kombination mit den integrierten Stilen verfügt das Dokument jetzt über acht Stile.
// Ein benutzerdefinierter Stil wird als „verwendet“ markiert, solange Text im Dokument vorhanden ist
// in diesem Stil formatiert. Das bedeutet, dass die 4 von uns hinzugefügten Stile derzeit nicht verwendet werden.
Assert.AreEqual(8, doc.Styles.Count);

// Einen benutzerdefinierten Zeichenstil und dann einen benutzerdefinierten Listenstil anwenden. Dadurch werden sie als „gebraucht“ markiert.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Jetzt gibt es einen unbenutzten Zeichenstil und einen unbenutzten Listenstil.
// Die Cleanup()-Methode kann bei Konfiguration mit einem CleanupOptions-Objekt auf nicht verwendete Stile abzielen und diese entfernen.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Durch das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wird, wird dieser erneut als „unbenutzt“ markiert.
// Führen Sie die Cleanup-Methode erneut aus, um sie zu entfernen.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Siehe auch

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
