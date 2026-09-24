---
title: "RevisionGroup"
linktitle: "RevisionGroup"
second_title: "Aspose.Words para Java"
description: "Representa un grupo de objetos Revision secuenciales en Java."
type: docs
weight: 582
url: /es/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Representa un grupo de objetos [Revision](../../com.aspose.words/revision/) secuenciales.

Para obtener más información, visite el artículo de documentación [ Track Changes in a Document ][Track Changes in a Document].

 **Examples:** 

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Métodos

| Método | Descripción |
| --- | --- |
| [getAuthor()](#getAuthor) | Obtiene el autor de este grupo de revisiones. |
| [getRevisionType()](#getRevisionType) | Obtiene el tipo de revisiones incluidas en este grupo. |
| [getText()](#getText) | Devuelve el texto insertado/eliminado/movido o la descripción del cambio de formato. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Obtiene el autor de este grupo de revisiones.

 **Examples:** 

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - El autor de este grupo de revisiones.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Obtiene el tipo de revisiones incluidas en este grupo.

 **Examples:** 

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - El tipo de revisiones incluidas en este grupo. El valor devuelto es uno de los constantes de [RevisionType](../../com.aspose.words/revisiontype/).
### getText() {#getText}
```
public String getText()
```


Devuelve el texto insertado/eliminado/movido o la descripción del cambio de formato.

 **Examples:** 

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Texto insertado/eliminado/movido o descripción del cambio de formato.
