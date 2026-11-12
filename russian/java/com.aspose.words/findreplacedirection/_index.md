---
title: "FindReplaceDirection"
linktitle: "FindReplaceDirection"
second_title: "Aspose.Words для Java"
description: "Указывает направление для операций замены в Java."
type: docs
weight: 313
url: /ru/java/com.aspose.words/findreplacedirection/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceDirection
```

Указывает направление для операций замены.

 **Examples:** 

Показывает, как определить, в каком направлении проходит операция поиска и замены по документу.

```

 public void direction(int findReplaceDirection) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("Match 1.");
     builder.writeln("Match 2.");
     builder.writeln("Match 3.");
     builder.writeln("Match 4.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementRecorder callback = new TextReplacementRecorder();
     options.setReplacingCallback(callback);

     // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
     // operation to start from the end of the range, and traverse back to the beginning.
     // Set the "Direction" property to "FindReplaceDirection.Forward" to get the find-and-replace
     // operation to start from the beginning of the range, and traverse to the end.
     options.setDirection(findReplaceDirection);

     doc.getRange().replace(Pattern.compile("Match \\d*"), "Replacement", options);

     Assert.assertEquals("Replacement.\r" +
             "Replacement.\r" +
             "Replacement.\r" +
             "Replacement.", doc.getText().trim());

     switch (findReplaceDirection) {
         case FindReplaceDirection.FORWARD:
             Assert.assertEquals(new String[]{"Match 1", "Match 2", "Match 3", "Match 4"}, callback.getMatches().toArray());
             break;
         case FindReplaceDirection.BACKWARD:
             Assert.assertEquals(new String[]{"Match 4", "Match 3", "Match 2", "Match 1"}, callback.getMatches().toArray());
             break;
     }
 }

 public static Object[][] directionDataProvider() {
     return new Object[][]
             {
                     {FindReplaceDirection.BACKWARD},
                     {FindReplaceDirection.FORWARD},
             };
 }

 /// 
 /// Records all matches that occur during a find-and-replace operation in the order that they take place.
 /// 
 private static class TextReplacementRecorder implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(0));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }
     private ArrayList mMatches = new ArrayList<>();
 }
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BACKWARD](#BACKWARD) | Совпадающие элементы заменяются от последнего к первому. |
| [FORWARD](#FORWARD) | Совпадающие элементы заменяются от первого к последнему. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String findReplaceDirectionName)](#fromName-java.lang.String) |  |
| [getName(int findReplaceDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int findReplaceDirection)](#toString-int) |  |
### BACKWARD {#BACKWARD}
```
public static int BACKWARD
```


Совпадающие элементы заменяются от последнего к первому.

### FORWARD {#FORWARD}
```
public static int FORWARD
```


Совпадающие элементы заменяются от первого к последнему.

### length {#length}
```
public static int length
```


### fromName(String findReplaceDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String findReplaceDirectionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| findReplaceDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int findReplaceDirection) {#getName-int}
```
public static String getName(int findReplaceDirection)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| findReplaceDirection | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int findReplaceDirection) {#toString-int}
```
public static String toString(int findReplaceDirection)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| findReplaceDirection | int |  |

**Returns:**
java.lang.String
