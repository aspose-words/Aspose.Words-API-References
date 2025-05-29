---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder PopFont-metoden för att enkelt återställa teckenformatering från stacken och förbättra din dokumentskapandeprocess.
type: docs
weight: 630
url: /sv/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Hämtar teckenformatering som tidigare sparats på stacken.

```csharp
public void PopFont()
```

## Exempel

Visar hur man använder formateringsstack för ett dokumentverktyg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in teckensnittsformatering och skriv sedan texten som kommer före hyperlänken.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Bevara vår nuvarande formateringskonfiguration på stacken.
builder.PushFont();

// Ändra verktygets nuvarande formatering genom att använda en ny stil.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", falskt);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Återställ teckensnittsformateringen som vi sparade tidigare och ta bort elementet från stacken.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Se även

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
