---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words pour Java"
description: "Implémentez cette interface pour fournir le style de bibliographie aux champs FieldBibliography et FieldCitation lorsqu'ils sont mis à jour en Java."
type: docs
weight: 753
url: /fr/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Implémentez cette interface pour fournir le style de bibliographie aux champs [FieldBibliography](../../com.aspose.words/fieldbibliography/) et [FieldCitation](../../com.aspose.words/fieldcitation/) lorsqu'ils sont mis à jour.

 **Examples:** 

Montre comment remplacer les styles intégrés ou fournir un style personnalisé.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```
## Méthodes

| Méthode | Description |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Renvoie le style de bibliographie. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Renvoie le style de bibliographie.

 **Remarks:** 

L'implémentation doit renvoyer  null  pour indiquer que la version MS Word du style spécifié doit être utilisée.

 **Examples:** 

Montre comment remplacer les styles intégrés ou fournir un style personnalisé.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| styleFileName | java.lang.String | Le nom de fichier du style de bibliographie. |

**Returns:**
java.io.InputStream - Le java.io.InputStream avec une feuille de style XSLT de style bibliographique.
