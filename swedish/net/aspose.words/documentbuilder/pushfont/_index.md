---
title: DocumentBuilder.PushFont
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Sparar aktuell teckenformatering i stacken.
type: docs
weight: 610
url: /sv/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Sparar aktuell teckenformatering i stacken.

```csharp
public void PushFont()
```

### Exempel

Visar hur du använder en dokumentbyggares formateringsstack.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in teckensnittsformatering och skriv sedan texten som går före hyperlänken.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Bevara vår nuvarande formateringskonfiguration i stacken.
builder.PushFont();

// Ändra byggarens nuvarande formatering genom att använda en ny stil.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

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
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


