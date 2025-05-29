---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words für .NET
description: Steuern Sie Seitenumbrüche mit der ForcePageBreaks-Eigenschaft von TxtSaveOptionsBase. Sorgen Sie für nahtlose Exporte und behalten Sie die Dokumentformatierung mühelos bei.
type: docs
weight: 30
url: /de/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Ermöglicht die Angabe, ob die Seitenumbrüche beim Export erhalten bleiben sollen.

Der Standardwert ist`FALSCH`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Bemerkungen

Die Eigenschaft betrifft nur Seitenumbrüche, die explizit in ein Dokument eingefügt werden. Sie hat keinen Bezug zu Seitenumbrüchen, die MS Word automatisch am Ende jeder Seite einfügt.

## Beispiele

Zeigt, wie Sie angeben, ob Seitenumbrüche beim Exportieren eines Dokuments in Klartext beibehalten werden sollen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die Funktion "Speichern" des Dokuments übergeben können.
// Methode zum Ändern der Art und Weise, wie wir das Dokument im Klartext speichern.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Die Aspose.Words-„Dokument“-Objekte haben Seitenumbrüche, genau wie Microsoft Word-Dokumente.
// Speicherformate wie „.txt“ sind ein fortlaufender Textkörper ohne Seitenumbrüche.
// Setzen Sie die Eigenschaft „ForcePageBreaks“ auf „true“, um alle Seitenumbrüche in Form von „\f“-Zeichen beizubehalten.
// Setzen Sie die Eigenschaft „ForcePageBreaks“ auf „false“, um alle Seitenumbrüche zu verwerfen.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Wenn wir ein Klartextdokument mit Seitenumbrüchen laden,
// Das Objekt „Dokument“ verwendet sie, um den Textkörper in Seiten aufzuteilen.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Siehe auch

* class [TxtSaveOptionsBase](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
