---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words für .NET
description: PageSetup BorderSurroundsHeader eigendom. Gibt an ob der Seitenrand die Kopfzeile einschließt oder ausschließt in C#.
type: docs
weight: 70
url: /de/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Gibt an, ob der Seitenrand die Kopfzeile einschließt oder ausschließt.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Bemerkungen

Beachten Sie, dass sich die Änderung dieser Eigenschaft auf alle Abschnitte im Dokument auswirkt.

## Beispiele

Zeigt, wie man einen Rahmen auf die Seite und die Kopf-/Fußzeile anwendet.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Einen blauen Doppellinienrand einfügen.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// Das PageSetup-Objekt eines Abschnitts verfügt über die Flags „BorderSurroundsHeader“ und „BorderSurroundsFooter“, die bestimmen
// ob ein Seitenrand den Haupttext umgibt, einschließlich der Kopf- bzw. Fußzeile.
// Setzen Sie das Flag „BorderSurroundsHeader“ auf „true“, um den Header mit unserem Rand zu umgeben.
// und dann das Flag „BorderSurroundsFooter“ setzen, um die Fußzeile außerhalb des Rahmens zu belassen.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
