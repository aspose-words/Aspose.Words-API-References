---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words pour .NET
description: Enregistrez vos documents sans effort grâce à notre méthode d'enregistrement intelligente, en sélectionnant automatiquement le bon format en fonction de l'extension de fichier pour un stockage transparent.
type: docs
weight: 750
url: /fr/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

Enregistre le document dans un fichier. Détermine automatiquement le format d'enregistrement à partir de l'extension.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du document. Si un document portant le nom de fichier spécifié existe déjà, il est écrasé. |

### Return_Value

Informations complémentaires que vous pouvez éventuellement utiliser.

## Exemples

Montre comment ouvrir un document et le convertir en .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Montre comment convertir un PDF en .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Chargez le document PDF que nous venons d'enregistrer et convertissez-le en .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

### Voir également

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

Enregistre le document dans un fichier au format spécifié.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du document. Si un document portant le nom de fichier spécifié existe déjà, il est écrasé. |
| saveFormat | SaveFormat | Le format dans lequel enregistrer le document. |

### Return_Value

Informations complémentaires que vous pouvez éventuellement utiliser.

## Exemples

Montre comment convertir du format DOCX au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Voir également

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

Enregistre le document dans un fichier en utilisant les options d'enregistrement spécifiées.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du document. Si un document portant le nom de fichier spécifié existe déjà, il est écrasé. |
| saveOptions | SaveOptions | Spécifie les options qui contrôlent la façon dont le document est enregistré. Peut être`nul`. |

### Return_Value

Informations complémentaires que vous pouvez éventuellement utiliser.

## Exemples

Montre comment améliorer la qualité d'un document rendu avec SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

Montre comment convertir un PDF en .docx et personnaliser le processus d'enregistrement avec un objet SaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Chargez le document PDF que nous venons d'enregistrer et convertissez-le en .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Définissez la propriété « Mot de passe » pour crypter le document enregistré avec un mot de passe.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Montre comment restituer chaque page d'un document dans une image TIFF distincte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Définissez la propriété « PageSet » sur le numéro de la première page à partir de
    // à partir duquel commencer le rendu du document.
    options.PageSet = new PageSet(i);
    // Exporter la page à 2325x5325 pixels et 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Montre comment restituer une page d'un document en une image JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Définissez le « PageSet » sur « 1 » pour sélectionner la deuxième page via
// l'index de base zéro à partir duquel démarrer le rendu du document.
options.PageSet = new PageSet(1);

// Lorsque nous enregistrons le document au format JPEG, Aspose.Words ne rend qu'une seule page.
// Cette image contiendra une page à partir de la page deux,
// qui sera simplement la deuxième page du document original.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Définissez la propriété « JpegQuality » sur « 10 » pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus importants.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Définissez la propriété « JpegQuality » sur « 100 » pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une augmentation de la taille du fichier.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Montre comment convertir un document entier en PDF avec trois niveaux dans le plan du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer les titres des niveaux 1 à 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son titre respectif.
// Définissez la propriété « HeadingsOutlineLevels » sur « 4 » pour exclure tous les titres dont les niveaux sont supérieurs à 4 du plan.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si une entrée de plan comporte des entrées ultérieures d'un niveau supérieur entre elle-même et l'entrée suivante du même niveau ou d'un niveau inférieur,
// Une flèche apparaîtra à gauche de l'entrée. Cette entrée est le « propriétaire » de plusieurs « sous-entrées ».
// Dans notre document, les entrées de plan du 5ème niveau de titre sont des sous-entrées de la deuxième entrée de plan du 4ème niveau,
// les entrées de niveau 4 et 5 sont des sous-entrées de la deuxième entrée de niveau 3, et ainsi de suite.
// Dans le plan, nous pouvons cliquer sur la flèche de l'entrée « propriétaire » pour réduire/développer toutes ses sous-entrées.
// Définissez la propriété « ExpandedOutlineLevels » sur « 2 » pour développer automatiquement toutes les entrées de plan de niveau 2 et inférieur
// et réduire toutes les entrées de niveau 3 et supérieur lorsque nous ouvrons le document.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Voir également

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

Enregistre le document dans un flux en utilisant le format spécifié.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Flux où enregistrer le document. |
| saveFormat | SaveFormat | Le format dans lequel enregistrer le document. |

### Return_Value

Informations complémentaires que vous pouvez éventuellement utiliser.

## Exemples

Montre comment enregistrer un document dans un flux.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Vérifiez que le flux contient le document.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Montre comment enregistrer un document dans une image via un flux, puis lire l'image à partir de ce flux.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Relisez le flux dans une image.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### Voir également

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

Enregistre le document dans un flux en utilisant les options d'enregistrement spécifiées.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Flux où enregistrer le document. |
| saveOptions | SaveOptions | Spécifie les options qui contrôlent la façon dont le document est enregistré. Peut être`nul` . Si c'est le cas`nul`, le document sera enregistré au format binaire DOC. |

### Return_Value

Informations complémentaires que vous pouvez éventuellement utiliser.

## Exemples

Montre comment convertir uniquement certaines pages d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la manière dont cette méthode convertit le document en .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Définissez « PageIndex » sur « 1 » pour restituer une partie du document à partir de la deuxième page.
    options.PageSet = new PageSet(1);

    // Ce document contiendra une page à partir de la page deux, qui ne contiendra que la deuxième page.
    doc.Save(stream, options);
}
```

### Voir également

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

Envoie le document au navigateur client.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| response | HttpResponse | Objet de réponse où enregistrer le document. |
| fileName | String | Le nom du document qui apparaîtra dans le navigateur client. Le nom ne doit pas contenir de chemin. |
| contentDisposition | ContentDisposition | UN[`ContentDisposition`](../../contentdisposition/) la valeur that spécifie comment le document est présenté dans le navigateur client. |
| saveOptions | SaveOptions | Spécifie les options qui contrôlent la façon dont le document est enregistré. Peut être`nul`. |

### Return_Value

Informations complémentaires que vous pouvez éventuellement utiliser.

## Remarques

En interne, cette méthode enregistre d'abord dans un flux de mémoire, puis copie dans le flux de réponse car le flux de réponse ne prend pas en charge la recherche.

## Exemples

Montre comment effectuer un publipostage, puis enregistrer le document dans le navigateur client.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Envoyer le document au navigateur client.
//Lancé car HttpResponse est nul dans le test.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Nous devrons fermer cette réponse manuellement pour nous assurer que nous n'ajoutons aucun contenu superflu au document après l'enregistrement.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Voir également

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
