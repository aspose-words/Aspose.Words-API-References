---
title: HtmlLoadOptions.HtmlLoadOptions
second_title: Aspose.Words för .NET API Referens
description: HtmlLoadOptions byggare. Initierar en ny instans av denna klass med standardvärden.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Initierar en ny instans av denna klass med standardvärden.

```csharp
public HtmlLoadOptions()
```

### Exempel

Visar hur man stödjer villkorliga kommentarer när ett HTML-dokument laddas.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Om värdet är sant tar vi hänsyn till VML-koden när vi analyserar det laddade dokumentet.
loadOptions.SupportVml = supportVml;

// Detta dokument innehåller en JPEG-bild inom "<!--[if gte vml 1]>" taggar,
// och en annan PNG-bild inom "<![if !vml]>" taggar.
// Om vi ställer in "SupportVml"-flaggan till "true", kommer Aspose.Words att ladda JPEG.
// Om vi sätter denna flagga till "false", så kommer Aspose.Words bara att ladda PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../htmlloadoptions/)
* hopsättning [Aspose.Words](../../../)

---

## HtmlLoadOptions(string) {#constructor_2}

En genväg för att initiera en ny instans av denna klass med det angivna lösenordet för att ladda ett krypterat dokument.

```csharp
public HtmlLoadOptions(string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | String | Lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. |

### Exempel

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

// För att ladda och läsa det här dokumentet måste vi godkänna dess dekryptering
// lösenord med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../htmlloadoptions/)
* hopsättning [Aspose.Words](../../../)

---

## HtmlLoadOptions(LoadFormat, string, string) {#constructor_1}

En genväg för att initiera en ny instans av denna klass med egenskaper inställda på de angivna värdena.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| loadFormat | LoadFormat | Formatet på dokumentet som ska laddas. |
| password | String | Lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. |
| baseUri | String | Strängen som kommer att användas för att lösa relativa URI:er till absoluta. Kan vara`null` eller tom sträng. |

### Exempel

Visar hur du anger en bas-URI när du öppnar ett HTML-dokument.

```csharp
// Anta att vi vill ladda ett .html-dokument som innehåller en bild länkad av en relativ URI
// medan bilden är på en annan plats. I så fall måste vi lösa den relativa URI till en absolut.
 // Vi kan tillhandahålla en bas-URI med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Medan bilden var trasig i inmatningen .html, hjälpte vår anpassade bas-URI oss att reparera länken.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Detta utdatadokument visar bilden som saknades.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Se även

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../htmlloadoptions/)
* hopsättning [Aspose.Words](../../../)


