---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words for .NET
description: Discover the HtmlLoadOptions constructor, designed to effortlessly initialize instances with default settings for seamless web development.
type: docs
weight: 10
url: /net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Initializes a new instance of this class with default values.

```csharp
public HtmlLoadOptions()
```

## Examples

Shows how to support conditional comments while loading an HTML document.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// If the value is true, then we take VML code into account while parsing the loaded document.
loadOptions.SupportVml = supportVml;

// This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
// and a different PNG image within "<![if !vml]>" tags.
// If we set the "SupportVml" flag to "true", then Aspose.Words will load the JPEG.
// If we set this flag to "false", then Aspose.Words will only load the PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.That(((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType, Is.EqualTo(ImageType.Jpeg));
else
    Assert.That(((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType, Is.EqualTo(ImageType.Png));
```

### See Also

* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)

---

## HtmlLoadOptions(*string*) {#constructor_2}

A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.

```csharp
public HtmlLoadOptions(string password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | String | The password to open an encrypted document. Can be `null` or empty string. |

## Examples

Shows how to encrypt an Html document, and then open it using a password.

```csharp
// Create and sign an encrypted HTML document from an encrypted .docx.
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

// To load and read this document, we will need to pass its decryption
// password using a HtmlLoadOptions object.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.That(loadOptions.Password, Is.EqualTo(signOptions.DecryptionPassword));

Document doc = new Document(outputFileName, loadOptions);

Assert.That(doc.GetText().Trim(), Is.EqualTo("Test encrypted document."));
```

### See Also

* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)

---

## HtmlLoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

A shortcut to initialize a new instance of this class with properties set to the specified values.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | LoadFormat | The format of the document to be loaded. |
| password | String | The password to open an encrypted document. Can be `null` or empty string. |
| baseUri | String | The string that will be used to resolve relative URIs to absolute. Can be `null` or empty string. |

## Examples

Shows how to specify a base URI when opening an html document.

```csharp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object. 
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.That(loadOptions.LoadFormat, Is.EqualTo(LoadFormat.Html));

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.That(imageShape.IsImage, Is.True);

// This output document will display the image that was missing.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### See Also

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
