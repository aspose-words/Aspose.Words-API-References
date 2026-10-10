---
title: "PdfLoadOptions"
linktitle: "PdfLoadOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier des options supplémentaires lors du chargement d'un document Pdf dans un objet Document en Java."
type: docs
weight: 538
url: /fr/java/com.aspose.words/pdfloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class PdfLoadOptions extends LoadOptions
```

Permet de spécifier des options supplémentaires lors du chargement d'un document Pdf dans un objet [Document](../../com.aspose.words/document/).

Pour en savoir plus, visitez l'article de documentation [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [getBaseUri()](#getBaseUri) | Obtient la chaîne qui sera utilisée pour résoudre les URI relatives trouvées dans le document en URI absolues lorsque cela est nécessaire. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Obtient s'il faut convertir les images de métafichier (**F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) au format d'image **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Obtient s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [getEncoding()](#getEncoding) | Obtient l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. |
| [getFontSettings()](#getFontSettings) | Permet de spécifier les paramètres de police du document. |
| [getIgnoreOleData()](#getIgnoreOleData) | Spécifie s'il faut ignorer les données OLE. |
| [getLanguagePreferences()](#getLanguagePreferences) | Obtient les préférences linguistiques qui seront utilisées lors du chargement du document. |
| [getLoadFormat()](#getLoadFormat) | Spécifie le format du document à charger. |
| [getMswVersion()](#getMswVersion) | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. |
| [getPageCount()](#getPageCount) | Obtient le nombre de pages à lire. |
| [getPageIndex()](#getPageIndex) | Obtient l'index basé sur 0 de la première page à lire. |
| [getPassword()](#getPassword) | Obtient le mot de passe pour ouvrir un document chiffré. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Obtient s'il faut préserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | Appelé pendant le chargement d'un document et accepte les données concernant la progression du chargement. |
| [getRecoveryMode()](#getRecoveryMode) | Définit comment le document doit être traité si des erreurs surviennent lors du chargement. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [getSkipPdfImages()](#getSkipPdfImages) | Obtient le drapeau indiquant si les images doivent être ignorées lors du chargement du document PDF. |
| [getTempFolder()](#getTempFolder) | Permet d'utiliser des fichiers temporaires lors de la lecture du document. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Spécifie s'il faut mettre à jour les champs avec l'attribut  dirty . |
| [getUseSystemLcid()](#getUseSystemLcid) | Obtient s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page. |
| [getWarningCallback()](#getWarningCallback) | Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Définit la chaîne qui sera utilisée pour résoudre les URI relatives trouvées dans le document en URI absolues lorsque cela est nécessaire. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Définit s'il faut convertir les images de métafichier ( **F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) au format d'image **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Définit s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Permet de spécifier les paramètres de police du document. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Spécifie s'il faut ignorer les données OLE. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Spécifie le format du document à charger. |
| [setMswVersion(int value)](#setMswVersion-int) | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. |
| [setPageCount(int value)](#setPageCount-int) | Définit le nombre de pages à lire. |
| [setPageIndex(int value)](#setPageIndex-int) | Définit l'index basé sur 0 de la première page à lire. |
| [setPassword(String value)](#setPassword-java.lang.String) | Définit le mot de passe pour ouvrir un document chiffré. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Définit s'il faut préserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Appelé pendant le chargement d'un document et accepte les données concernant la progression du chargement. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Définit comment le document doit être traité si des erreurs surviennent lors du chargement. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [setSkipPdfImages(boolean value)](#setSkipPdfImages-boolean) | Définit le drapeau indiquant si les images doivent être ignorées lors du chargement du document PDF. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Permet d'utiliser des fichiers temporaires lors de la lecture du document. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Spécifie s'il faut mettre à jour les champs avec l'attribut  dirty . |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Définit s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Obtient la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire. Peut être  null  ou chaîne vide. La valeur par défaut est  null .

 **Remarks:** 

Cette propriété est utilisée pour résoudre les URI relatifs en absolus dans les cas suivants :

1.  Lors du chargement d'un document HTML à partir d'un flux et que le document contient des images avec des URI relatifs et n'a pas d'URI de base spécifié dans l'élément BASE du HTML.
2.  Lors de l'enregistrement d'un document au format PDF et autres formats, pour récupérer les images liées à l'aide d'URI relatifs afin que les images puissent être enregistrées dans le document de sortie.

 **Examples:** 

Montre comment ouvrir un document HTML avec des images à partir d'un flux en utilisant une URI de base.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Returns:**
java.lang.String - La chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire.
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Obtient s'il faut convertir les images de métafichier (**F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) au format d'image **F:Aspose.FileFormat.Png**.

 **Remarks:** 

Les métafichiers (**F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) sont un format d'image non compressé et nécessitent parfois trop de RAM pour contenir et traiter le document. Cette option permet de convertir toutes les images de métafichiers en **F:Aspose.FileFormat.Png** lors du chargement du document. Veuillez noter - la conversion des graphiques vectoriels en images raster diminue la qualité des images.

 **Examples:** 

Montre comment convertir WMF/EMF en PNG lors du chargement du document.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Returns:**
boolean - Indique s'il faut convertir les images de métafichiers (**F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) en format d'image **F:Aspose.FileFormat.Png**.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


Obtient s'il faut convertir les formes avec EquationXML en objets Office Math.

 **Examples:** 

Montre comment convertir les formes EquationXML en objets Office Math.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Returns:**
boolean - Indique s'il faut convertir les formes avec EquationXML en objets Office Math.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Obtient le codage qui sera utilisé pour charger un document HTML, TXT ou CHM si le codage n'est pas spécifié dans le document. Peut être  null . La valeur par défaut est  null .

 **Remarks:** 

Cette propriété n'est utilisée que lors du chargement de documents HTML, TXT ou CHM.

Si le codage n'est pas spécifié dans le document et que cette propriété est  null , le système tentera de détecter automatiquement le codage.

 **Examples:** 

Montre comment définir le codage avec lequel ouvrir un document.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Returns:**
java.nio.charset.Charset - Le codage qui sera utilisé pour charger un document HTML, TXT ou CHM si le codage n'est pas spécifié dans le document.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Permet de spécifier les paramètres de police du document.

 **Remarks:** 

Lors du chargement de certains formats, Aspose.Words peut devoir résoudre les polices. Par exemple, lors du chargement de documents HTML, Aspose.Words peut résoudre les polices pour effectuer le repli de police.

Si défini sur  null , les paramètres de police statiques par défaut [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) seront utilisés.

La valeur par défaut est  null .

 **Examples:** 

Montre comment désigner des substituts de police lors du chargement.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

Montre comment appliquer les paramètres de substitution de police lors du chargement d'un document.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getIgnoreOleData() {#getIgnoreOleData}
```
public boolean getIgnoreOleData()
```


Spécifie s'il faut ignorer les données OLE.

 **Remarks:** 

Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.

La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les données OLE lors du chargement.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Obtient les préférences linguistiques qui seront utilisées lors du chargement du document.

 **Examples:** 

Montre comment appliquer les préférences de langue lors du chargement d’un document.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```

**Returns:**
[LanguagePreferences](../../com.aspose.words/languagepreferences/) - Language preferences that will be used when document is loading.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Spécifie le format du document à charger. La valeur par défaut est [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Il est recommandé de spécifier la valeur [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) et de laisser Aspose.Words détecter automatiquement le format du fichier. Si vous connaissez le format du document que vous vous apprêtez à charger, vous pouvez spécifier le format explicitement, ce qui réduira légèrement le temps de chargement en évitant le surcoût lié à la détection automatique du format. Si vous spécifiez un format de chargement explicite et qu'il s'avère incorrect, la détection automatique sera invoquée et une seconde tentative de chargement du fichier sera effectuée.

 **Examples:** 

Montre comment spécifier une URI de base lors de l'ouverture d'un document html.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [LoadFormat](../../com.aspose.words/loadformat/).
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut est [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

Différentes versions de Word peuvent gérer certains aspects du contenu et du formatage du document légèrement différemment pendant le processus de chargement, ce qui peut entraîner de légères différences dans le modèle d'objet du document.

 **Examples:** 

Montre comment émuler la procédure de chargement d'une version spécifique de Microsoft Word lors du chargement du document.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [MsWordVersion](../../com.aspose.words/mswordversion/).
### getPageCount() {#getPageCount}
```
public int getPageCount()
```


Obtient le nombre de pages à lire. La valeur par défaut est MaxValue, ce qui signifie que toutes les pages du document seront lues.

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```

**Returns:**
int - Le nombre de pages à lire.
### getPageIndex() {#getPageIndex}
```
public int getPageIndex()
```


Obtient l'index basé sur 0 de la première page à lire. La valeur par défaut est 0.

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```

**Returns:**
int - L'index basé sur 0 de la première page à lire.
### getPassword() {#getPassword}
```
public String getPassword()
```


Obtient le mot de passe pour ouvrir un document chiffré. Peut être  null  ou une chaîne vide. La valeur par défaut est  null .

 **Remarks:** 

Vous devez connaître le mot de passe pour ouvrir un document chiffré. Si le document n'est pas chiffré, définissez-le sur  null  ou une chaîne vide.

 **Examples:** 

Montre comment signer un fichier de document chiffré.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
java.lang.String - Le mot de passe pour ouvrir un document chiffré.
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Obtient si le champ INCLUDEPICTURE doit être conservé lors de la lecture des formats Microsoft Word. La valeur par défaut est false.

 **Remarks:** 

Par défaut, le champ INCLUDEPICTURE est converti en un objet forme. Vous pouvez remplacer cela si vous avez besoin que le champ soit conservé, par exemple, si vous souhaitez le mettre à jour par programme. Notez toutefois que cette approche n'est pas courante pour Aspose.Words. Utilisez-la à vos propres risques.

Un des cas d'utilisation possibles peut être d'utiliser un MERGEFIELD comme champ enfant pour modifier dynamiquement le chemin source de l'image. Dans ce cas, vous devez que le champ INCLUDEPICTURE soit conservé dans le modèle.

 **Examples:** 

Montre comment conserver ou ignorer les champs INCLUDEPICTURE lors du chargement d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Returns:**
booléen - Indique si le champ INCLUDEPICTURE doit être conservé lors de la lecture des formats Microsoft Word.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Appelé pendant le chargement d'un document et accepte les données concernant la progression du chargement.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Montre comment notifier l'utilisateur si le chargement du document a dépassé le temps de chargement prévu.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Returns:**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) - The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) value.
### getRecoveryMode() {#getRecoveryMode}
```
public int getRecoveryMode()
```


Définit comment le document doit être géré si des erreurs surviennent pendant le chargement. Utilisez cette propriété pour spécifier si le système doit tenter de récupérer le document ou suivre un autre comportement défini. La valeur par défaut est [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Montre comment tenter de récupérer un document si des erreurs sont survenues pendant le chargement.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/).
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML.

 **Examples:** 

Montre comment gérer les ressources externes lors du chargement de documents Html.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value.
### getSkipPdfImages() {#getSkipPdfImages}
```
public boolean getSkipPdfImages()
```


Obtient le drapeau indiquant si les images doivent être ignorées lors du chargement du document PDF. La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```

**Returns:**
boolean - Le drapeau indiquant si les images doivent être ignorées lors du chargement du document PDF.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est null et aucun fichier temporaire n'est utilisé.

 **Remarks:** 

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires lorsque la lecture est terminée.

 **Examples:** 

Montre comment charger un document en utilisant des fichiers temporaires.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Montre comment utiliser le disque dur au lieu de la mémoire lors du chargement d'un document.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Spécifie s'il faut mettre à jour les champs avec l'attribut  dirty .

 **Examples:** 

Montre comment utiliser la propriété spéciale pour mettre à jour le résultat du champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Obtient s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page.

 **Remarks:** 

Si défini sur true, le comportement de MS Word est émulé, ce qui prend la valeur LCID du registre Windows.

La valeur par défaut est false.

**Returns:**
booléen - Indique s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage.

 **Examples:** 

Montre comment afficher et enregistrer les avertissements qui surviennent lors du chargement du document.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Définit la chaîne qui sera utilisée pour résoudre les URI relatives trouvées dans le document en URI absolues lorsque cela est nécessaire. Peut être null ou une chaîne vide. La valeur par défaut est null.

 **Remarks:** 

Cette propriété est utilisée pour résoudre les URI relatifs en absolus dans les cas suivants :

1.  Lors du chargement d'un document HTML à partir d'un flux et que le document contient des images avec des URI relatifs et n'a pas d'URI de base spécifié dans l'élément BASE du HTML.
2.  Lors de l'enregistrement d'un document au format PDF et autres formats, pour récupérer les images liées à l'aide d'URI relatifs afin que les images puissent être enregistrées dans le document de sortie.

 **Examples:** 

Montre comment ouvrir un document HTML avec des images à partir d'un flux en utilisant une URI de base.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Définit s'il faut convertir les images de métafichier ( **F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) au format d'image **F:Aspose.FileFormat.Png**.

 **Remarks:** 

Les métafichiers (**F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) sont un format d'image non compressé et nécessitent parfois trop de RAM pour contenir et traiter le document. Cette option permet de convertir toutes les images de métafichiers en **F:Aspose.FileFormat.Png** lors du chargement du document. Veuillez noter - la conversion des graphiques vectoriels en images raster diminue la qualité des images.

 **Examples:** 

Montre comment convertir WMF/EMF en PNG lors du chargement du document.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique s'il faut convertir les images de métafichier ( **F:Aspose.FileFormat.Wmf** ou **F:Aspose.FileFormat.Emf**) au format d'image **F:Aspose.FileFormat.Png**. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Définit s'il faut convertir les formes avec EquationXML en objets Office Math.

 **Examples:** 

Montre comment convertir les formes EquationXML en objets Office Math.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique s'il faut convertir les formes contenant EquationXML en objets Office Math. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être  null . La valeur par défaut est  null .

 **Remarks:** 

Cette propriété n'est utilisée que lors du chargement de documents HTML, TXT ou CHM.

Si le codage n'est pas spécifié dans le document et que cette propriété est  null , le système tentera de détecter automatiquement le codage.

 **Examples:** 

Montre comment définir le codage avec lequel ouvrir un document.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.nio.charset.Charset | L'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Permet de spécifier les paramètres de police du document.

 **Remarks:** 

Lors du chargement de certains formats, Aspose.Words peut devoir résoudre les polices. Par exemple, lors du chargement de documents HTML, Aspose.Words peut résoudre les polices pour effectuer le repli de police.

Si défini sur  null , les paramètres de police statiques par défaut [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) seront utilisés.

La valeur par défaut est  null .

 **Examples:** 

Montre comment désigner des substituts de police lors du chargement.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

Montre comment appliquer les paramètres de substitution de police lors du chargement d'un document.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | La valeur correspondante de [FontSettings](../../com.aspose.words/fontsettings/). |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


Spécifie s'il faut ignorer les données OLE.

 **Remarks:** 

Ignorer les données OLE peut réduire la consommation de mémoire et augmenter les performances sans perte de données dans le cas où le format de destination ne prend pas en charge les objets OLE.

La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les données OLE lors du chargement.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Spécifie le format du document à charger. La valeur par défaut est [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Il est recommandé de spécifier la valeur [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) et de laisser Aspose.Words détecter automatiquement le format du fichier. Si vous connaissez le format du document que vous vous apprêtez à charger, vous pouvez spécifier le format explicitement, ce qui réduira légèrement le temps de chargement en évitant le surcoût lié à la détection automatique du format. Si vous spécifiez un format de chargement explicite et qu'il s'avère incorrect, la détection automatique sera invoquée et une seconde tentative de chargement du fichier sera effectuée.

 **Examples:** 

Montre comment spécifier une URI de base lors de l'ouverture d'un document html.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [LoadFormat](../../com.aspose.words/loadformat/). |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut est [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

Différentes versions de Word peuvent gérer certains aspects du contenu et du formatage du document légèrement différemment pendant le processus de chargement, ce qui peut entraîner de légères différences dans le modèle d'objet du document.

 **Examples:** 

Montre comment émuler la procédure de chargement d'une version spécifique de Microsoft Word lors du chargement du document.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [MsWordVersion](../../com.aspose.words/mswordversion/). |

### setPageCount(int value) {#setPageCount-int}
```
public void setPageCount(int value)
```


Définit le nombre de pages à lire. La valeur par défaut est MaxValue, ce qui signifie que toutes les pages du document seront lues.

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le nombre de pages à lire. |

### setPageIndex(int value) {#setPageIndex-int}
```
public void setPageIndex(int value)
```


Définit l'index basé sur 0 de la première page à lire. La valeur par défaut est 0.

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | L'index basé sur 0 de la première page à lire. |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Définit le mot de passe pour ouvrir un document chiffré. Peut être  null  ou une chaîne vide. La valeur par défaut est  null .

 **Remarks:** 

Vous devez connaître le mot de passe pour ouvrir un document chiffré. Si le document n'est pas chiffré, définissez-le sur  null  ou une chaîne vide.

 **Examples:** 

Montre comment signer un fichier de document chiffré.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le mot de passe pour ouvrir un document chiffré. |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est  false .

 **Remarks:** 

Par défaut, le champ INCLUDEPICTURE est converti en un objet forme. Vous pouvez remplacer cela si vous avez besoin que le champ soit conservé, par exemple, si vous souhaitez le mettre à jour par programme. Notez toutefois que cette approche n'est pas courante pour Aspose.Words. Utilisez-la à vos propres risques.

Un des cas d'utilisation possibles peut être d'utiliser un MERGEFIELD comme champ enfant pour modifier dynamiquement le chemin source de l'image. Dans ce cas, vous devez que le champ INCLUDEPICTURE soit conservé dans le modèle.

 **Examples:** 

Montre comment conserver ou ignorer les champs INCLUDEPICTURE lors du chargement d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Appelé pendant le chargement d'un document et accepte les données concernant la progression du chargement.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Montre comment notifier l'utilisateur si le chargement du document a dépassé le temps de chargement prévu.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | La valeur correspondante [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/). |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


Définit comment le document doit être géré si des erreurs surviennent pendant le chargement. Utilisez cette propriété pour spécifier si le système doit tenter de récupérer le document ou suivre un autre comportement défini. La valeur par défaut est [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Montre comment tenter de récupérer un document si des erreurs sont survenues pendant le chargement.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/). |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML.

 **Examples:** 

Montre comment gérer les ressources externes lors du chargement de documents Html.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | La valeur correspondante [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/). |

### setSkipPdfImages(boolean value) {#setSkipPdfImages-boolean}
```
public void setSkipPdfImages(boolean value)
```


Définit le drapeau indiquant si les images doivent être ignorées lors du chargement du document PDF. La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les images lors du chargement de fichiers PDF.

```

 PdfLoadOptions options = new PdfLoadOptions();
 options.setSkipPdfImages(isSkipPdfImages);
 options.setPageIndex(0);
 options.setPageCount(1);

 Document doc = new Document(getMyDir() + "Images.pdf", options);
 NodeCollection shapeCollection = doc.getChildNodes(NodeType.SHAPE, true);

 if (isSkipPdfImages)
     Assert.assertEquals(shapeCollection.getCount(), 0);
 else
     Assert.assertNotEquals(shapeCollection.getCount(), 0);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Le drapeau indiquant si les images doivent être ignorées lors du chargement du document PDF. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est null et aucun fichier temporaire n'est utilisé.

 **Remarks:** 

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires lorsque la lecture est terminée.

 **Examples:** 

Montre comment charger un document en utilisant des fichiers temporaires.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Montre comment utiliser le disque dur au lieu de la mémoire lors du chargement d'un document.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Spécifie s'il faut mettre à jour les champs avec l'attribut  dirty .

 **Examples:** 

Montre comment utiliser la propriété spéciale pour mettre à jour le résultat du champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Définit s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page.

 **Remarks:** 

Si défini sur true, le comportement de MS Word est émulé, ce qui prend la valeur LCID du registre Windows.

La valeur par défaut est false.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage.

 **Examples:** 

Montre comment afficher et enregistrer les avertissements qui surviennent lors du chargement du document.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | La valeur correspondante de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

