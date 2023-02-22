---
title: LoadOptions.Encoding
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ruft die Kodierung ab oder legt sie fest die verwendet wird um ein HTML TXT oder CHMDokument zu laden wenn die Kodierung nicht innerhalb des Dokuments angegeben ist. Kann null sein. Standard ist null.
type: docs
weight: 50
url: /de/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Ruft die Kodierung ab oder legt sie fest, die verwendet wird, um ein HTML-, TXT- oder CHM-Dokument zu laden, wenn die Kodierung nicht innerhalb des Dokuments angegeben ist. Kann null sein. Standard ist null.

```csharp
public Encoding Encoding { get; set; }
```

### Bemerkungen

Diese Eigenschaft wird nur beim Laden von HTML-, TXT- oder CHM-Dokumenten verwendet.

Wenn die Codierung nicht im Dokument angegeben ist und diese Eigenschaft ist`Null`, dann versucht das System, die Kodierung automatisch zu erkennen.

### Beispiele

Zeigt, wie Sie die Codierung festlegen, mit der ein Dokument geöffnet werden soll.

```csharp
// Ein FileFormatInfo-Objekt erkennt, dass diese Datei in etwas anderem als UTF-7 codiert ist.
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Encoded in UTF-7.txt");

Assert.AreNotEqual(Encoding.UTF7, fileFormatInfo.Encoding);

// Wenn wir das Dokument ohne Ladekonfigurationen laden, erkennt Aspose.Words seine Kodierung als UTF-8.
Document doc = new Document(MyDir + "Encoded in UTF-7.txt");

// Der in UTF-8 geparste Inhalt erzeugt einen gültigen String.
// Da wir jedoch wissen, dass die Datei in UTF-7 vorliegt, können wir sehen, dass das Ergebnis falsch ist.
Assert.AreEqual("Hello world+ACE-", doc.ToString(SaveFormat.Text).Trim());

// Bei mehrdeutiger Kodierung wie dieser können wir eine bestimmte Kodierungsvariante einstellen
// um die Datei innerhalb eines LoadOptions-Objekts zu parsen.
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.UTF7
};

// Laden Sie das Dokument, während Sie das LoadOptions-Objekt übergeben, und überprüfen Sie dann den Inhalt des Dokuments.
doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);

Assert.AreEqual("Hello world!", doc.ToString(SaveFormat.Text).Trim());
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


