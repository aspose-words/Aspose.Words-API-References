---
title: "ListLabel"
linktitle: "ListLabel"
second_title: "Aspose.Words для Java"
description: "Определяет свойства, специфичные для метки списка в Java."
type: docs
weight: 428
url: /ru/java/com.aspose.words/listlabel/
---

**Inheritance:**
java.lang.Object
```
public class ListLabel
```

Определяет свойства, специфичные для метки списка.

Чтобы узнать больше, посетите статью документации [ Working with Lists ][Working with Lists].

 **Examples:** 

Показывает, как извлечь метки списка из всех абзацев, являющихся элементами списка.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Методы

| Метод | Описание |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getFont()](#getFont) | Получает шрифт метки списка. |
| [getLabelString()](#getLabelString) | Получает строковое представление метки списка. |
| [getLabelValue()](#getLabelValue) | Получает числовое значение этой метки. |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getFont() {#getFont}
```
public Font getFont()
```


Получает шрифт метки списка.

**Returns:**
[Font](../../com.aspose.words/font/) - The list label font.
### getLabelString() {#getLabelString}
```
public String getLabelString()
```


Получает строковое представление метки списка.

 **Examples:** 

Показывает, как извлечь метки списка из всех абзацев, являющихся элементами списка.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
java.lang.String - Строковое представление метки списка.
### getLabelValue() {#getLabelValue}
```
public int getLabelValue()
```


Получает числовое значение этой метки.

 **Remarks:** 

Используйте метод [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) для обновления значения этого свойства.

 **Examples:** 

Показывает, как извлечь метки списка из всех абзацев, являющихся элементами списка.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
int - Числовое значение этой метки.
### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |
| значение | java.lang.Object |  |

