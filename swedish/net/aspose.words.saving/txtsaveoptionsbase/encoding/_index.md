---
title: TxtSaveOptionsBase.Encoding
second_title: Aspose.Words för .NET API Referens
description: TxtSaveOptionsBase fast egendom. Anger kodningen som ska användas vid export i textformat. Standardvärdet är Encoding.UTF8 .
type: docs
weight: 10
url: /sv/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Anger kodningen som ska användas vid export i textformat. Standardvärdet är **Encoding.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

### Exempel

Visar hur man ställer in kodning för ett .txt-utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till lite text med tecken utanför ASCII-teckenuppsättningen.
builder.Write("À È Ì Ò Ù.");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Verifiera att egenskapen "Encoding" innehåller lämplig kodning för vårt dokuments innehåll.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// Att använda en olämplig kodning kan resultera i att dokumentinnehållet går förlorat.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### Se även

* class [TxtSaveOptionsBase](../)
* namnutrymme [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* hopsättning [Aspose.Words](../../../)


