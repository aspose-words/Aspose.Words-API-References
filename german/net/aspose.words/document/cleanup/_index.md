---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit unserer Cleanup-Methode – entfernen Sie ungenutzte Formatvorlagen und Listen für einen saubereren und effizienteren Workflow. Verbessern Sie noch heute die Lesbarkeit!
type: docs
weight: 580
url: /de/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Löscht nicht verwendete Stile und Listen aus dem Dokument.

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

// Zusammen mit den integrierten Stilen verfügt das Dokument jetzt über acht Stile.
// Ein benutzerdefinierter Stil gilt als „verwendet“, wenn er auf einen Teil des Dokuments angewendet wird.
// was bedeutet, dass die vier von uns hinzugefügten Stile derzeit nicht verwendet werden.
Assert.AreEqual(8, doc.Styles.Count);

// Wenden Sie einen benutzerdefinierten Zeichenstil und dann einen benutzerdefinierten Listenstil an. Dadurch werden die Stile als "verwendet" markiert.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// Durch das Entfernen aller Knoten, auf die ein benutzerdefinierter Stil angewendet wird, werden diese wieder als „unbenutzt“ markiert.
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

Löscht nicht verwendete Stile und Listen aus dem Dokument, abhängig von der gegebenen[`CleanupOptions`](../../cleanupoptions/) .

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

// Zusammen mit den integrierten Stilen verfügt das Dokument jetzt über acht Stile.
// Ein benutzerdefinierter Stil wird als "verwendet" markiert, solange sich im Dokument Text befindet
// in diesem Stil formatiert. Dies bedeutet, dass die 4 hinzugefügten Stile derzeit nicht verwendet werden.
Assert.AreEqual(8, doc.Styles.Count);

// Wenden Sie einen benutzerdefinierten Zeichenstil und dann einen benutzerdefinierten Listenstil an. Dadurch werden sie als "verwendet" markiert.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Jetzt gibt es einen nicht verwendeten Zeichenstil und einen nicht verwendeten Listenstil.
// Die Cleanup()-Methode kann, wenn sie mit einem CleanupOptions-Objekt konfiguriert ist, nicht verwendete Stile gezielt ansprechen und entfernen.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

    // Durch das Entfernen aller Knoten, auf die ein benutzerdefinierter Stil angewendet wird, werden diese wieder als „unbenutzt“ markiert.
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
