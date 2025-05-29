---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die TxtSaveOptions-Eigenschaft „AddBidiMarks“ den Nur-Text-Export verbessert, indem sie bidirektionale Markierungen für verbesserte Lesbarkeit und Formatierung hinzufügt.
type: docs
weight: 20
url: /de/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Gibt an, ob beim Exportieren im Nur-Text-Format vor jedem BiDi-Lauf bidirektionale Markierungen hinzugefügt werden sollen.

Der Standardwert ist`FALSCH`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Beispiele

Zeigt, wie vor jedem bidirektionalen Lauf im Text das Unicode-Zeichen „RECHTS-NACH-LINKS-MARKIERUNG“ (U+200F) eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Setzen Sie die Eigenschaft „AddBidiMarks“ auf „true“, um vor dem Ausführen Markierungen hinzuzufügen
// mit Text von rechts nach links, um die Tatsache anzuzeigen.
// Setzen Sie die Eigenschaft „AddBidiMarks“ auf „false“, um alles von links nach rechts zu schreiben
// und von rechts nach links verlaufen sie gleichmäßig, ohne dass etwas darauf hinweist, was was ist.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Siehe auch

* class [TxtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
