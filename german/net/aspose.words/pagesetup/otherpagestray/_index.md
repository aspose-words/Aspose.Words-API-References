---
title: PageSetup.OtherPagesTray
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft das Papierfach Ablagefach ab das für alle außer der ersten Seite eines Abschnitts verwendet werden soll oder legt es fest. Der Wert ist ImplementierungsDruckerspezifisch.
type: docs
weight: 300
url: /de/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Ruft das Papierfach (Ablagefach) ab, das für alle außer der ersten Seite eines Abschnitts verwendet werden soll, oder legt es fest. Der Wert ist Implementierungs-(Drucker-)spezifisch.

```csharp
public int OtherPagesTray { get; set; }
```

### Beispiele

Zeigt, wie alle Abschnitte in einem Dokument dazu gebracht werden, das Standardpapierfach des ausgewählten Druckers zu verwenden.

```csharp
Document doc = new Document();

// Finden Sie den Standarddrucker, den wir zum Drucken dieses Dokuments verwenden werden.
// Sie können einen bestimmten Drucker mithilfe der Eigenschaft „PrinterName“ des PrinterSettings-Objekts definieren.
PrinterSettings settings = new PrinterSettings();

// Der in Dokumenten gespeicherte Papierfachwert ist druckerspezifisch.
// Dies bedeutet, dass der folgende Code alle Seitenfachwerte zurücksetzt, um das aktuelle Standardfach des Druckers zu verwenden.
// Sie können PrinterSettings.PaperSources auflisten, um die anderen gültigen Papierfachwerte des ausgewählten Druckers zu finden.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Zeigt, wie das Drucken mit verschiedenen Druckerfächern für unterschiedliche Papierformate eingerichtet wird.

```csharp
Document doc = new Document();

// Finden Sie den Standarddrucker, den wir zum Drucken dieses Dokuments verwenden werden.
// Sie können einen bestimmten Drucker mithilfe der Eigenschaft „PrinterName“ des PrinterSettings-Objekts definieren.
PrinterSettings settings = new PrinterSettings();

// Dies ist das Fach, das wir für Seiten im Papierformat „A4“ verwenden.
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Dies ist das Fach, das wir für Seiten im Papierformat „Letter“ verwenden.
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Ändern Sie das PageSettings-Objekt dieses Abschnitts, damit Microsoft Word den Drucker anweist
// um je nach Papierformat dieses Abschnitts eines der oben identifizierten Fächer zu verwenden.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


