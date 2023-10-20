---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.CleanupOptions klas. Ermöglicht die Angabe von Optionen für die Dokumentenbereinigung in C#.
type: docs
weight: 210
url: /de/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Ermöglicht die Angabe von Optionen für die Dokumentenbereinigung.

Um mehr zu erfahren, besuchen Sie die[Bereinigen Sie ein Dokument](https://docs.aspose.com/words/net/clean-up-a-document/) Dokumentationsartikel.

```csharp
public class CleanupOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Ruft/setzt ein Flag, das angibt, ob doppelte Stile aus dem Dokument entfernt werden sollen. Der Standardwert ist`FALSCH` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Gibt an, dass es nicht verwendet wird[`BuiltIn`](../style/builtin/) Stile sollten aus dem Dokument entfernt werden. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Gibt an, ob nicht verwendete Listen und Listendefinitionen aus dem Dokument entfernt werden sollen. Der Standardwert ist`WAHR` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Gibt an, ob nicht verwendete Stile aus dem Dokument entfernt werden sollen. Der Standardwert ist`WAHR` . |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
