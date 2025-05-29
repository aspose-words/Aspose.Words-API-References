---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.CleanupOptions, um die Dokumentenbereinigung anzupassen. Verbessern Sie Ihren Workflow mit maßgeschneiderten Einstellungen für sauberere, effizientere Dokumente.
type: docs
weight: 400
url: /de/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Ermöglicht die Angabe von Optionen zur Dokumentbereinigung.

Um mehr zu erfahren, besuchen Sie die[Bereinigen eines Dokuments](https://docs.aspose.com/words/net/clean-up-a-document/) Dokumentationsartikel.

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
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Ruft ein Flag ab/setzt es, das angibt, ob doppelte Stile aus dem Dokument entfernt werden sollen. Der Standardwert ist`FALSCH` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Gibt an, dass nicht verwendete[`BuiltIn`](../style/builtin/) Stile sollten aus dem Dokument entfernt werden. |
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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
