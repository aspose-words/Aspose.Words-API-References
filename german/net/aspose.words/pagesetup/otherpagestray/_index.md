---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup OtherPagesTray-Funktion, um die Papierfacheinstellungen Ihres Druckers einfach anzupassen. Optimieren Sie die Druckeffizienz für jeden Abschnitt!
type: docs
weight: 300
url: /de/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Ruft das Papierfach (Bin) ab, das für alle Seiten eines Abschnitts außer der ersten verwendet werden soll, oder legt es fest. Der Wert ist implementierungsspezifisch (druckerspezifisch).

```csharp
public int OtherPagesTray { get; set; }
```

## Beispiele

Zeigt, wie Sie dafür sorgen, dass alle Abschnitte eines Dokuments das Standardpapierfach des ausgewählten Druckers verwenden.

```csharp
Document doc = new Document();

// Suchen Sie den Standarddrucker, den wir zum Drucken dieses Dokuments verwenden werden.
// Sie können einen bestimmten Drucker mithilfe der Eigenschaft „PrinterName“ des PrinterSettings-Objekts definieren.
PrinterSettings settings = new PrinterSettings();

// Der in Dokumenten gespeicherte Papierfachwert ist druckerspezifisch.
// Dies bedeutet, dass der folgende Code alle Seitenfachwerte zurücksetzt, um das aktuelle Standardfach des Druckers zu verwenden.
// Sie können PrinterSettings.PaperSources aufzählen, um die anderen gültigen Papierfachwerte des ausgewählten Druckers zu finden.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Zeigt, wie der Druckvorgang mit unterschiedlichen Druckerfächern für unterschiedliche Papiergrößen eingerichtet wird.

```csharp
Document doc = new Document();

// Suchen Sie den Standarddrucker, den wir zum Drucken dieses Dokuments verwenden werden.
// Sie können einen bestimmten Drucker mithilfe der Eigenschaft „PrinterName“ des PrinterSettings-Objekts definieren.
PrinterSettings settings = new PrinterSettings();

// Dies ist das Fach, das wir für Seiten im Papierformat „A4“ verwenden werden.
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Dies ist das Fach, das wir für Seiten im Papierformat „Letter“ verwenden werden.
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Ändern Sie das PageSettings-Objekt dieses Abschnitts, damit Microsoft Word den Drucker anweist
// um je nach Papiergröße dieses Abschnitts eines der oben angegebenen Fächer zu verwenden.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
