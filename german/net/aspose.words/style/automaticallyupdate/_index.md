---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words für .NET
description: Style AutomaticallyUpdate eigendom. Gibt an ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird in C#.
type: docs
weight: 20
url: /de/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Bemerkungen

Wenn der Eigenschaftswert auf „true“ gesetzt ist, definiert MS Word den aktuellen Stil automatisch neu, wenn die entsprechende Absatzformatierung geändert wurde.

Die Eigenschaft „Automatisch aktualisieren“ gilt nur für Absatzstile.

Der Standardwert ist`FALSCH`.

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

// Einen der Stile aus dem Dokument auf den Absatz anwenden, den der Dokumentersteller erstellt.
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
