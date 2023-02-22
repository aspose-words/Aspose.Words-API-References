---
title: TxtSaveOptions.AddBidiMarks
second_title: Aspose.Words für .NET-API-Referenz
description: TxtSaveOptions eigendom. Gibt an ob bidirektionale Markierungen vor jedem BiDiLauf hinzugefügt werden sollen wenn im NurTextFormat exportiert wird.
type: docs
weight: 20
url: /de/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Gibt an, ob bidirektionale Markierungen vor jedem BiDi-Lauf hinzugefügt werden sollen, wenn im Nur-Text-Format exportiert wird.

Der Standardwert ist **FALSCH**.

```csharp
public bool AddBidiMarks { get; set; }
```

### Beispiele

Zeigt, wie das Unicode-Zeichen „RIGHT-TO-LEFT MARK“ (U+200F) vor jedem bidirektionalen Run in Text eingefügt wird.

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

// Setzen Sie die Eigenschaft "AddBidiMarks" auf "true", um Markierungen vor den Läufen hinzuzufügen
// mit Text von rechts nach links, um die Tatsache anzuzeigen.
// Setzen Sie die Eigenschaft "AddBidiMarks" auf "false", um alles von links nach rechts zu schreiben
// und rechts-nach-links verlaufen gleich, ohne anzuzeigen, was was ist.
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
* namensraum [Aspose.Words.Saving](../../txtsaveoptions/)
* Montage [Aspose.Words](../../../)


