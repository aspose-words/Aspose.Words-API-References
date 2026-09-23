---
title: "PreferredWidth"
linktitle: "PreferredWidth"
second_title: "Aspose.Words pour Java"
description: "Représente une valeur et son unité de mesure utilisées pour spécifier la largeur préférée d'un tableau ou d'une cellule en Java."
type: docs
weight: 550
url: /fr/java/com.aspose.words/preferredwidth/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidth
```

Représente une valeur et son unité de mesure utilisées pour spécifier la largeur préférée d'un tableau ou d'une cellule.

Pour en savoir plus, consultez l'article de documentation [ Working with Tables ][Working with Tables].

 **Remarks:** 

La largeur préférée peut être spécifiée en pourcentage, en nombre de points ou avec une valeur spéciale "none/auto".

Les instances de cette classe sont immuables.

 **Examples:** 

Montre comment ajuster automatiquement un tableau à 50% de la largeur de la page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Renvoie une instance qui représente la valeur "largeur préférée non spécifiée". |
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth) | Détermine si le [PreferredWidth](../../com.aspose.words/preferredwidth/) spécifié est égal en valeur au [PreferredWidth](../../com.aspose.words/preferredwidth/) actuel. |
| [equals(Object obj)](#equals-java.lang.Object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [fromPercent(double percent)](#fromPercent-double) | Une méthode de création qui renvoie une nouvelle instance représentant une largeur préférée spécifiée en pourcentage. |
| [fromPoints(double points)](#fromPoints-double) | Une méthode de création qui renvoie une nouvelle instance représentant une largeur préférée spécifiée en nombre de points. |
| [getType()](#getType) | Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée. |
| [getValue()](#getValue) | Obtient la valeur de largeur préférée. |
| [hashCode()](#hashCode) |  |
| [toString()](#toString) | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


Renvoie une instance qui représente la valeur "largeur préférée non spécifiée".

 **Examples:** 

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth}
```
public boolean equals(PreferredWidth other)
```


Détermine si le [PreferredWidth](../../com.aspose.words/preferredwidth/) spécifié est égal en valeur au [PreferredWidth](../../com.aspose.words/preferredwidth/) actuel.

 **Examples:** 

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

 **Examples:** 

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromPercent(double percent) {#fromPercent-double}
```
public static PreferredWidth fromPercent(double percent)
```


Une méthode de création qui renvoie une nouvelle instance représentant une largeur préférée spécifiée en pourcentage.

 **Examples:** 

Montre comment ajuster automatiquement un tableau à 50% de la largeur de la page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pourcentage | double | La valeur doit être comprise entre 0 et 100. |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### fromPoints(double points) {#fromPoints-double}
```
public static PreferredWidth fromPoints(double points)
```


Une méthode de création qui renvoie une nouvelle instance représentant une largeur préférée spécifiée en nombre de points.

 **Examples:** 

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

Montre comment utiliser les outils de conversion d'unités tout en spécifiant une largeur préférée pour une cellule.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(ConvertUtil.inchToPoint(3.0)));
 builder.insertCell();

 Assert.assertEquals(216.0d, table.getFirstRow().getFirstCell().getCellFormat().getPreferredWidth().getValue());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| points | double | La valeur doit être comprise entre 0 et 22 pouces (22 \* 72 points). |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### getType() {#getType}
```
public int getType()
```


Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée.

 **Examples:** 

Montre comment vérifier le type et la valeur de la largeur préférée d’une cellule de tableau.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
int - L'unité de mesure utilisée pour cette valeur de largeur préférée. La valeur renvoyée est l'une des constantes [PreferredWidthType](../../com.aspose.words/preferredwidthtype/).
### getValue() {#getValue}
```
public double getValue()
```


Obtient la valeur de largeur préférée. L'unité de mesure est spécifiée dans la propriété [getType()](../../com.aspose.words/preferredwidth/\#getType).

 **Examples:** 

Montre comment vérifier le type et la valeur de la largeur préférée d’une cellule de tableau.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
double - La valeur de largeur préférée.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```


Renvoie une chaîne conviviale qui affiche la valeur de cet objet.

 **Examples:** 

Montre comment définir une largeur préférée pour les cellules de tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Returns:**
java.lang.String
