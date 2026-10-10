---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words para Java"
description: "Proporciona banderas de configuración para la operación de unión de ejecuciones en Java."
type: docs
weight: 406
url: /es/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Proporciona banderas de configuración para la operación de unión de ejecuciones.

 **Examples:** 

Muestra cómo unir ejecuciones con el mismo formato mientras se ignoran los atributos redundantes e insignificantes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True indica que los atributos insignificantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True indica que los atributos redundantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True indica que los atributos de espaciado de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True indica que los atributos insignificantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True indica que los atributos redundantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True indica que los atributos de espaciado de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True indica que los atributos insignificantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato.

 **Remarks:** 

Los atributos insignificantes son aquellos atributos que no tienen un efecto notable en el formato de una ejecución con el contenido de texto dado. El valor predeterminado es False.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True indica que los atributos redundantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato.

 **Remarks:** 

Los atributos redundantes son aquellos atributos que no afectan la ejecución con el contenido de texto dado. El valor predeterminado es False.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True indica que los atributos de espaciado de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato.

 **Remarks:** 

El valor predeterminado es False.

**Returns:**
boolean - El valor  boolean  correspondiente.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True indica que los atributos insignificantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato.

 **Remarks:** 

Los atributos insignificantes son aquellos atributos que no tienen un efecto notable en el formato de una ejecución con el contenido de texto dado. El valor predeterminado es False.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True indica que los atributos redundantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato.

 **Remarks:** 

Los atributos redundantes son aquellos atributos que no afectan la ejecución con el contenido de texto dado. El valor predeterminado es False.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True indica que los atributos de espaciado de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato.

 **Remarks:** 

El valor predeterminado es False.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

