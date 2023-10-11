---
title: TxtSaveOptionsBase.ForcePageBreaks
second_title: Aspose.Words für .NET-API-Referenz
description: TxtSaveOptionsBase eigendom. Ermöglicht die Angabe ob die Seitenumbrüche beim Export beibehalten werden sollen.
type: docs
weight: 30
url: /de/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Ermöglicht die Angabe, ob die Seitenumbrüche beim Export beibehalten werden sollen.

Der Standardwert ist`FALSCH`.

```csharp
public bool ForcePageBreaks { get; set; }
```

### Bemerkungen

Die Eigenschaft betrifft nur Seitenumbrüche, die explizit in ein Dokument eingefügt werden. Es hat nichts mit Seitenumbrüchen zu tun, die MS Word automatisch am Ende jeder Seite einfügt.

### Beispiele

Zeigt, wie Sie angeben, ob Seitenumbrüche beim Exportieren eines Dokuments in Klartext beibehalten werden sollen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Erstellen Sie ein „TxtSaveOptions“-Objekt, das wir an den „Speichern“ des Dokuments übergeben können.
// Methode zum Ändern der Art und Weise, wie wir das Dokument im Klartext speichern.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Die „Document“-Objekte von Aspose.Words verfügen über Seitenumbrüche, genau wie Microsoft Word-Dokumente.
// Speicherformate wie „.txt“ sind ein fortlaufender Textkörper ohne Seitenumbrüche.
// Setzen Sie die Eigenschaft „ForcePageBreaks“ auf „true“, um alle Seitenumbrüche in Form von „\f“-Zeichen beizubehalten.
// Setzen Sie die Eigenschaft „ForcePageBreaks“ auf „false“, um alle Seitenumbrüche zu verwerfen.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Wenn wir ein Klartextdokument mit Seitenumbrüchen laden,
// Das Objekt „Dokument“ verwendet sie, um den Hauptteil in Seiten aufzuteilen.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Siehe auch

* class [TxtSaveOptionsBase](../)
* namensraum [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* Montage [Aspose.Words](../../../)


