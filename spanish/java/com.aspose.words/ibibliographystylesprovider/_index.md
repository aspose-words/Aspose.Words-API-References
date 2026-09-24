---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words para Java"
description: "Implemente esta interfaz para proporcionar el estilo de bibliografía para los campos FieldBibliography y FieldCitation cuando se actualicen en Java."
type: docs
weight: 753
url: /es/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Implemente esta interfaz para proporcionar el estilo de bibliografía para los campos [FieldBibliography](../../com.aspose.words/fieldbibliography/) y [FieldCitation](../../com.aspose.words/fieldcitation/) cuando se actualicen.

 **Examples:** 

Muestra cómo sobrescribir estilos incorporados o proporcionar uno personalizado.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Devuelve el estilo de bibliografía. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Devuelve el estilo de bibliografía.

 **Remarks:** 

La implementación debe devolver  null  para indicar que se debe usar la versión de MS Word del estilo especificado.

 **Examples:** 

Muestra cómo sobrescribir estilos incorporados o proporcionar uno personalizado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| styleFileName | java.lang.String | El nombre de archivo del estilo de bibliografía. |

**Returns:**
java.io.InputStream - El java.io.InputStream con hoja de estilo XSLT de estilo bibliográfico.
