---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die PageSetup BorderSurroundsFooter-Eigenschaft Ihr Dokumentlayout verbessern kann, indem sie die Einbindung der Fußzeile in die Seitenränder steuert.
type: docs
weight: 60
url: /de/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Gibt an, ob der Seitenrand die Fußzeile einschließt oder nicht.

```csharp
public bool BorderSurroundsFooter { get; set; }
```

## Bemerkungen

Beachten Sie, dass sich das Ändern dieser Eigenschaft auf alle Abschnitte im Dokument auswirkt.

## Beispiele

Zeigt, wie Sie der Seite und der Kopf-/Fußzeile einen Rahmen hinzufügen.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Fügen Sie einen blauen Doppellinienrahmen ein.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// Das PageSetup-Objekt eines Abschnitts verfügt über die Flags "BorderSurroundsHeader" und "BorderSurroundsFooter", die bestimmen
// ob ein Seitenrahmen den Haupttext umgibt, schließt auch die Kopf- bzw. Fußzeile ein.
// Setzen Sie das Flag „BorderSurroundsHeader“ auf „true“, um den Header mit unserem Rahmen zu umgeben,
// und setzen Sie dann das Flag „BorderSurroundsFooter“, um die Fußzeile außerhalb des Rahmens zu belassen.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
