---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos unerwünschte Stile aus Ihrem Dokument mit der Methode „Stil entfernen“. Verbessern Sie das Erscheinungsbild Ihrer Inhalte und sorgen Sie für Konsistenz!
type: docs
weight: 230
url: /de/net/aspose.words/style/remove/
---
## Style.Remove method

Entfernt den angegebenen Stil aus dem Dokument.

```csharp
public void Remove()
```

## Bemerkungen

Das Entfernen von Stilen hat folgende Auswirkungen auf das Dokumentmodell:

* Sämtliche Stilverweise werden aus den entsprechenden Absätzen, Absätzen und Tabellen entfernt.
* Wenn der Basisstil entfernt wird, wird seine Formatierung in die untergeordneten Stile verschoben.
* Wenn der zu löschende Stil einen verknüpften Stil hat, werden beide gelöscht.

## Beispiele

Zeigt, wie ein benutzerdefinierter Stil erstellt und angewendet wird.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Stil automatisch neu definieren.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Wenden Sie einen der Stile aus dem Dokument auf den Absatz an, den der Dokumentgenerator erstellt.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Entfernen Sie unseren benutzerdefinierten Stil aus der Stilsammlung des Dokuments.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Jeder Text, der einen entfernten Stil verwendet hat, wird auf die Standardformatierung zurückgesetzt.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Siehe auch

* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
