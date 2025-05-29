---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck HtmlLoadOptions-konstruktorn, utformad för att enkelt initiera instanser med standardinställningar för sömlös webbutveckling.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Initierar en ny instans av den här klassen med standardvärden.

```csharp
public HtmlLoadOptions()
```

## Exempel

Visar hur man stöder villkorsstyrda kommentarer när man laddar ett HTML-dokument.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Om värdet är sant tar vi hänsyn till VML-kod när vi analyserar det inlästa dokumentet.
loadOptions.SupportVml = supportVml;

// Detta dokument innehåller en JPEG-bild inom taggarna "<!--[if gte vml 1]>",
// och en annan PNG-bild inom taggarna "<![if !vml]>".
// Om vi ställer in flaggan "SupportVml" till "true", så kommer Aspose.Words att ladda JPEG-filen.
// Om vi ställer in denna flagga till "false", kommer Aspose.Words bara att ladda PNG-filen.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)

---

## HtmlLoadOptions(*string*) {#constructor_2}

En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument.

```csharp
public HtmlLoadOptions(string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | String | Lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. |

## Exempel

Visar hur man krypterar ett HTML-dokument och sedan öppnar det med ett lösenord.

```csharp
// Skapa och signera ett krypterat HTML-dokument från en krypterad .docx.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// För att ladda och läsa detta dokument måste vi dekryptera det
// lösenord med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)

---

## HtmlLoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

En genväg för att initiera en ny instans av den här klassen med egenskaper inställda på de angivna värdena.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| loadFormat | LoadFormat | Formatet på dokumentet som ska laddas. |
| password | String | Lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. |
| baseUri | String | Strängen som ska användas för att lösa relativa URI:er till absoluta värden. Kan vara`null` eller tom sträng. |

## Exempel

Visar hur man anger en bas-URI när man öppnar ett HTML-dokument.

```csharp
// Anta att vi vill ladda ett .html-dokument som innehåller en bild länkad av en relativ URI
// medan bilden är på en annan plats. I så fall måste vi omvandla den relativa URI:n till en absolut.
 // Vi kan tillhandahålla en bas-URI med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Även om bilden i indata-.html-filen var trasig, hjälpte vår anpassade bas-URI oss att reparera länken.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Detta utdatadokument visar bilden som saknades.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Se även

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
