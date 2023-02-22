---
title: Document.Cleanup
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Entfernt ungenutzte Stile und Listen aus dem Dokument.
type: docs
weight: 520
url: /de/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Entfernt ungenutzte Stile und Listen aus dem Dokument.

```csharp
public void Cleanup()
```

### Beispiele

Zeigt, wie Sie nicht verwendete benutzerdefinierte Stile aus einem Dokument entfernen.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Kombiniert mit den eingebauten Stilen hat das Dokument jetzt acht Stile.
// Ein benutzerdefinierter Stil gilt als "verwendet", während er auf einen Teil des Dokuments angewendet wird,
// was bedeutet, dass die vier hinzugefügten Stile derzeit nicht verwendet werden.
Assert.AreEqual(8, doc.Styles.Count);

// Anwenden eines benutzerdefinierten Zeichenstils und dann eines benutzerdefinierten Listenstils. Dadurch werden die Stile als "verwendet" markiert.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// Das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wird, markiert ihn wieder als "unbenutzt".
// Führen Sie die Cleanup-Methode erneut aus, um sie zu entfernen.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Cleanup(CleanupOptions) {#cleanup_1}

Entfernt ungenutzte Stile und Listen je nach Vorgabe aus dem Dokument[`CleanupOptions`](../../cleanupoptions/) .

```csharp
public void Cleanup(CleanupOptions options)
```

### Beispiele

Zeigt, wie alle nicht verwendeten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Kombiniert mit den eingebauten Stilen hat das Dokument jetzt acht Stile.
// Ein benutzerdefinierter Stil wird als "verwendet" markiert, solange Text im Dokument vorhanden ist
// in diesem Stil formatiert. Das bedeutet, dass die 4 von uns hinzugefügten Stile derzeit nicht verwendet werden.
Assert.AreEqual(8, doc.Styles.Count);

// Anwenden eines benutzerdefinierten Zeichenstils und dann eines benutzerdefinierten Listenstils. Dadurch werden sie als "benutzt" markiert.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Jetzt gibt es einen unbenutzten Zeichenstil und einen unbenutzten Listenstil.
// Die Cleanup()-Methode kann, wenn sie mit einem CleanupOptions-Objekt konfiguriert ist, auf ungenutzte Stile abzielen und sie entfernen.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

// Das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wird, markiert ihn wieder als "unbenutzt". 
// Führen Sie die Cleanup-Methode erneut aus, um sie zu entfernen.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Siehe auch

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


