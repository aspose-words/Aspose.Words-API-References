---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words per Java"
description: "Implementa questa interfaccia per fornire lo stile bibliografico per i campi FieldBibliography e FieldCitation quando vengono aggiornati in Java."
type: docs
weight: 753
url: /it/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Implementa questa interfaccia per fornire lo stile bibliografico per i campi [FieldBibliography](../../com.aspose.words/fieldbibliography/) e [FieldCitation](../../com.aspose.words/fieldcitation/) quando vengono aggiornati.

 **Examples:** 

Mostra come sovrascrivere gli stili predefiniti o fornire uno personalizzato.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Restituisce lo stile bibliografico. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Restituisce lo stile bibliografico.

 **Remarks:** 

L'implementazione dovrebbe restituire  null  per indicare che dovrebbe essere utilizzata la versione MS Word dello stile specificato.

 **Examples:** 

Mostra come sovrascrivere gli stili predefiniti o fornire uno personalizzato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| styleFileName | java.lang.String | Il nome file dello stile bibliografico. |

**Returns:**
java.io.InputStream - Il java.io.InputStream con foglio di stile XSLT per bibliografia.
