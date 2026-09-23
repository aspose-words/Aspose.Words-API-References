---
title: "ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words для Java"
description: "Представляет все форматирование абзаца в Java."
type: docs
weight: 525
url: /ru/java/com.aspose.words/paragraphformat/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphFormat
```

Представляет всё форматирование абзаца.

Чтобы узнать больше, посетите статью документации [ Working with Paragraphs ][Working with Paragraphs].

 **Examples:** 

Показывает, как вручную создать документ Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Сбрасывает форматирование абзаца к значениям по умолчанию. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha) | Получает флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами латинского текста и регионами восточноазиатского текста в текущем абзаце. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit) | Получает флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами чисел и регионами восточноазиатского текста в текущем абзаце. |
| [getAlignment()](#getAlignment) | Получает выравнивание текста для абзаца. |
| [getBaselineAlignment()](#getBaselineAlignment) | Получает вертикальное положение шрифтов на строке. |
| [getBidi()](#getBidi) | Получает, является ли данный абзац направленным справа налево. |
| [getBorders()](#getBorders) | Получает коллекцию границ абзаца. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent) | Получает значение (в символах) для отступа первой строки или висячего отступа. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent) | Получает значение левого отступа (в символах) для указанных абзацев. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent) | Получает значение правого отступа (в символах) для указанных абзацев. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDropCapPosition()](#getDropCapPosition) | Получает позицию для текста буквицы. |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl) | Получает флаг, указывающий, применяются ли правила разрыва строк восточноазиатского текста к текущему абзацу. |
| [getFirstLineIndent()](#getFirstLineIndent) | Получает значение (в пунктах) для первой строки или висячего отступа. |
| [getHangingPunctuation()](#getHangingPunctuation) | Получает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |
| [getKeepTogether()](#getKeepTogether) | Истина, если все строки в абзаце должны оставаться на одной странице. |
| [getKeepWithNext()](#getKeepWithNext) | Истина, если абзац должен оставаться на той же странице, что и следующий за ним абзац. |
| [getLeftIndent()](#getLeftIndent) | Возвращает значение (в пунктах), представляющее левый отступ абзаца. |
| [getLineSpacing()](#getLineSpacing) | Возвращает межстрочный интервал (в пунктах) для абзаца. |
| [getLineSpacingRule()](#getLineSpacingRule) | Возвращает межстрочный интервал для абзаца. |
| [getLineUnitAfter()](#getLineUnitAfter) | Возвращает количество интервала (в сеточных линиях) после абзацев. |
| [getLineUnitBefore()](#getLineUnitBefore) | Возвращает количество интервала (в сеточных линиях) перед абзацами. |
| [getLinesToDrop()](#getLinesToDrop) | Возвращает количество строк текста абзаца, используемых для вычисления высоты буквицы. |
| [getMirrorIndents()](#getMirrorIndents) | Возвращает флаг, указывающий, одинаковы ли ширины левого и правого отступов. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle) | Когда true, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) и [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) будут игнорироваться между абзацами одного и того же стиля. |
| [getOutlineLevel()](#getOutlineLevel) | Указывает уровень структуры абзаца в документе. |
| [getPageBreakBefore()](#getPageBreakBefore) | Истина, если перед абзацем принудительно вставлен разрыв страницы. |
| [getRightIndent()](#getRightIndent) | Возвращает значение (в пунктах), представляющее правый отступ абзаца. |
| [getShading()](#getShading) | Возвращает объект [Shading](../../com.aspose.words/shading/), который относится к форматированию затенения абзаца. |
| [getSnapToGrid()](#getSnapToGrid) | Указывает, следует ли текущему абзацу использовать настройки сеточных линий документа на страницу при размещении содержимого в абзаце. |
| [getSpaceAfter()](#getSpaceAfter) | Возвращает количество интервала (в пунктах) после абзаца. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto) | Истина, если количество интервала после абзаца задаётся автоматически. |
| [getSpaceBefore()](#getSpaceBefore) | Возвращает количество интервала (в пунктах) перед абзацем. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto) | Истина, если количество интервала перед абзацем задаётся автоматически. |
| [getStyle()](#getStyle) | Возвращает стиль абзаца, применённый к этому форматированию. |
| [getStyleIdentifier()](#getStyleIdentifier) | Возвращает независимый от локали идентификатор стиля абзаца, применённый к этому форматированию. |
| [getStyleName()](#getStyleName) | Возвращает название стиля абзаца, применённого к этому форматированию. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens) | Указывает, следует ли освобождать текущий абзац от любой переноски, применяемой в настройках документа. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers) | Указывает, следует ли освобождать строки текущего абзаца от нумерации строк, применяемой в родительском разделе. |
| [getTabStops()](#getTabStops) | Возвращает коллекцию пользовательских табуляций, определённых для этого объекта. |
| [getWidowControl()](#getWidowControl) | Истина, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца. |
| [getWordWrap()](#getWordWrap) | Если это свойство ложно, латинский текст в середине слова может переноситься в текущем абзаце. |
| [isHeading()](#isHeading) | Истина, когда стиль абзаца является одним из встроенных стилей заголовков. |
| [isListItem()](#isListItem) | Истина, когда абзац является элементом маркированного или нумерованного списка. |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean) | Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями текста восточноазиатского языка в текущем абзаце. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean) | Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями текста восточноазиатского языка в текущем абзаце. |
| [setAlignment(int value)](#setAlignment-int) | Устанавливает выравнивание текста для абзаца. |
| [setBaselineAlignment(int value)](#setBaselineAlignment-int) | Устанавливает вертикальное положение шрифтов в строке. |
| [setBidi(boolean value)](#setBidi-boolean) | Устанавливает, является ли этот абзац направленным справа налево. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double) | Устанавливает значение (в символах) для первой строки или висячего отступа. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double) | Устанавливает значение левого отступа (в символах) для указанных абзацев. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double) | Устанавливает значение правого отступа (в символах) для указанных абзацев. |
| [setDropCapPosition(int value)](#setDropCapPosition-int) | Устанавливает позицию текста с инициалом. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean) | Устанавливает флаг, указывающий, применяются ли правила переноса строк восточноазиатского текста к текущему абзацу. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double) | Устанавливает значение (в пунктах) для первой строки или висячего отступа. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean) | Устанавливает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean) | Истина, если все строки в абзаце должны оставаться на одной странице. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean) | Истина, если абзац должен оставаться на той же странице, что и следующий за ним абзац. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Устанавливает значение (в пунктах), представляющее левый отступ абзаца. |
| [setLineSpacing(double value)](#setLineSpacing-double) | Устанавливает межстрочный интервал (в пунктах) для абзаца. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int) | Устанавливает межстрочный интервал для абзаца. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double) | Устанавливает величину интервала (в сеточных линиях) после абзацев. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double) | Устанавливает величину интервала (в сеточных линиях) перед абзацами. |
| [setLinesToDrop(int value)](#setLinesToDrop-int) | Устанавливает количество строк текста абзаца, используемых для расчёта высоты инициалов. |
| [setMirrorIndents(boolean value)](#setMirrorIndents-boolean) | Устанавливает флаг, указывающий, одинаковой ли ширины левый и правый отступы. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean) | Когда true, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) и [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) будут игнорироваться между абзацами одного и того же стиля. |
| [setOutlineLevel(int value)](#setOutlineLevel-int) | Указывает уровень структуры абзаца в документе. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean) | Истина, если перед абзацем принудительно вставлен разрыв страницы. |
| [setRightIndent(double value)](#setRightIndent-double) | Устанавливает значение (в пунктах), представляющее правый отступ абзаца. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Указывает, следует ли текущему абзацу использовать настройки сеточных линий документа на страницу при размещении содержимого в абзаце. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Устанавливает величину интервала (в пунктах) после абзаца. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean) | Истина, если количество интервала после абзаца задаётся автоматически. |
| [setSpaceBefore(double value)](#setSpaceBefore-double) | Устанавливает величину отступа (в пунктах) перед абзацем. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean) | Истина, если количество интервала перед абзацем задаётся автоматически. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Устанавливает стиль абзаца, применяемый к этому форматированию. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Устанавливает независимый от локали идентификатор стиля абзаца, применяемый к этому форматированию. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Устанавливает имя стиля абзаца, применяемого к этому форматированию. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean) | Указывает, следует ли освобождать текущий абзац от любой переноски, применяемой в настройках документа. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean) | Указывает, следует ли освобождать строки текущего абзаца от нумерации строк, применяемой в родительском разделе. |
| [setWidowControl(boolean value)](#setWidowControl-boolean) | Истина, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца. |
| [setWordWrap(boolean value)](#setWordWrap-boolean) | Если это свойство ложно, латинский текст в середине слова может переноситься в текущем абзаце. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Сбрасывает форматирование абзаца к значениям по умолчанию.

 **Remarks:** 

Форматирование абзаца по умолчанию — стиль Normal, выравнивание по левому краю, без отступов, без интервалов, без границ и без заливки.

 **Examples:** 

Показывает, как вложить список в другой список.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


Получает флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами латинского текста и регионами восточноазиатского текста в текущем абзаце.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
boolean — Флаг, указывающий, автоматически ли регулируется межсимвольный интервал между участками латинского текста и участками восточноазиатского текста в текущем абзаце.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


Получает флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами чисел и регионами восточноазиатского текста в текущем абзаце.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
boolean — Флаг, указывающий, автоматически ли регулируется межсимвольный интервал между участками чисел и участками восточноазиатского текста в текущем абзаце.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Получает выравнивание текста для абзаца.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

Показывает, как вручную создать документ Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int — Выравнивание текста в абзаце. Возвращаемое значение является одной из констант [ParagraphAlignment](../../com.aspose.words/paragraphalignment/).
### getBaselineAlignment() {#getBaselineAlignment}
```
public int getBaselineAlignment()
```


Получает вертикальное положение шрифтов на строке.

 **Examples:** 

Показывает, как установить вертикальное положение шрифтов в строке.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```

**Returns:**
int — Вертикальное положение шрифтов в строке. Возвращаемое значение является одной из констант [BaselineAlignment](../../com.aspose.words/baselinealignment/).
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Получает, является ли данный абзац направленным справа налево.

 **Remarks:** 

Когда  true , элементы и другие встроенные объекты в этом абзаце размещаются справа налево.

 **Examples:** 

Показывает, как создавать списки, совместимые с языками справа налево, с помощью полей BIDIOUTLINE.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
 // but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
 // The following field will display ".1", the RTL equivalent of list number "1.".
 FieldBidiOutline field = (FieldBidiOutline) builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 Assert.assertEquals(" BIDIOUTLINE ", field.getFieldCode());

 // Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 // Set the horizontal text alignment for every paragraph in the document to RTL.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().setBidi(true);
 }

 // If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
 // Otherwise, they will display "###".
 doc.save(getArtifactsDir() + "Field.BIDIOUTLINE.docx");
 
```

Показывает, как определить направление текста в простом документе.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Returns:**
boolean — Является ли этот абзац правосторонним (right-to-left).
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Получает коллекцию границ абзаца.

 **Examples:** 

Показывает, как вставить абзац с верхней границей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - Collection of borders of the paragraph.
### getCharacterUnitFirstLineIndent() {#getCharacterUnitFirstLineIndent}
```
public double getCharacterUnitFirstLineIndent()
```


Получает значение (в символах) для отступа первой строки или висячего отступа.

Используйте положительные значения для установки отступа первой строки и отрицательные значения для установки висячего отступа.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double — Значение (в символах) для отступа первой строки или висячего отступа.
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent}
```
public double getCharacterUnitLeftIndent()
```


Получает значение левого отступа (в символах) для указанных абзацев.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double — Значение левого отступа (в символах) для указанных абзацев.
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent}
```
public double getCharacterUnitRightIndent()
```


Получает значение правого отступа (в символах) для указанных абзацев.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double — Значение правого отступа (в символах) для указанных абзацев.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### getDropCapPosition() {#getDropCapPosition}
```
public int getDropCapPosition()
```


Получает позицию для текста буквицы.

 **Examples:** 

Показывает, как вложить список в другой список.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
int — Позиция текста с буквицей. Возвращаемое значение является одной из констант [DropCapPosition](../../com.aspose.words/dropcapposition/).
### getFarEastLineBreakControl() {#getFarEastLineBreakControl}
```
public boolean getFarEastLineBreakControl()
```


Получает флаг, указывающий, применяются ли правила разрыва строк восточноазиатского текста к текущему абзацу.

 **Examples:** 

Показывает, как задать специальные свойства для азиатской типографии.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, применяются ли правила разрыва строк для восточноазиатского текста к текущему абзацу.
### getFirstLineIndent() {#getFirstLineIndent}
```
public double getFirstLineIndent()
```


Получает значение (в пунктах) для первой строки или висячего отступа.

Используйте положительные значения для установки отступа первой строки и отрицательные значения для установки висячего отступа.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
double — Значение (в пунктах) для первой строки или висячего отступа.
### getHangingPunctuation() {#getHangingPunctuation}
```
public boolean getHangingPunctuation()
```


Получает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

 **Examples:** 

Показывает, как задать специальные свойства для азиатской типографии.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.
### getKeepTogether() {#getKeepTogether}
```
public boolean getKeepTogether()
```


Истина, если все строки в абзаце должны оставаться на одной странице.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getKeepWithNext() {#getKeepWithNext}
```
public boolean getKeepWithNext()
```


Истина, если абзац должен оставаться на той же странице, что и следующий за ним абзац.

 **Examples:** 

Показывает, как установить таблицу так, чтобы она оставалась вместе на одной странице.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Возвращает значение (в пунктах), представляющее левый отступ абзаца.

 **Examples:** 

Показывает, как настроить форматирование абзаца для создания текста со смещением от центра.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Returns:**
double — Значение (в пунктах), представляющее левый отступ абзаца.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Возвращает межстрочный интервал (в пунктах) для абзаца.

 **Remarks:** 

Когда свойство [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) установлено в [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST), межстрочный интервал может быть больше или равен, но никогда не меньше указанного значения [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

Когда свойство [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) установлено в [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY), межстрочный интервал никогда не меняется от указанного значения [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), даже если в абзаце используется более крупный шрифт.

 **Examples:** 

Показывает, как работать с межстрочным интервалом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Returns:**
double - Межстрочный интервал (в пунктах) для абзаца.
### getLineSpacingRule() {#getLineSpacingRule}
```
public int getLineSpacingRule()
```


Возвращает межстрочный интервал для абзаца.

 **Examples:** 

Показывает, как работать с межстрочным интервалом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Returns:**
int - Межстрочный интервал для абзаца. Возвращаемое значение является одним из констант [LineSpacingRule](../../com.aspose.words/linespacingrule/).
### getLineUnitAfter() {#getLineUnitAfter}
```
public double getLineUnitAfter()
```


Возвращает количество интервала (в сеточных линиях) после абзацев.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - Количество интервала (в линиях сетки) после абзацев.
### getLineUnitBefore() {#getLineUnitBefore}
```
public double getLineUnitBefore()
```


Возвращает количество интервала (в сеточных линиях) перед абзацами.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - Количество интервала (в линиях сетки) перед абзацами.
### getLinesToDrop() {#getLinesToDrop}
```
public int getLinesToDrop()
```


Возвращает количество строк текста абзаца, используемых для вычисления высоты буквицы.

 **Examples:** 

Показывает, как задать размер буквицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
 // which will turn it into a large capital letter that will decorate the next paragraph.
 // Give this property a value of 4 to give the drop cap the height of four text lines.
 builder.getParagraphFormat().setLinesToDrop(4);
 builder.writeln("H");

 // Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
 // The text in this paragraph will wrap around the drop cap.
 builder.getParagraphFormat().setLinesToDrop(0);
 builder.writeln("ello world!");

 doc.save(getArtifactsDir() + "ParagraphFormat.LinesToDrop.odt");
 
```

**Returns:**
int - Количество строк текста абзаца, используемых для вычисления высоты буквицы.
### getMirrorIndents() {#getMirrorIndents}
```
public boolean getMirrorIndents()
```


Возвращает флаг, указывающий, одинаковы ли ширины левого и правого отступов.

 **Examples:** 

Показывает, как сделать одинаковыми отступы слева и справа.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Returns:**
boolean - Флаг, указывающий, одинаковы ли отступы слева и справа.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


Когда true, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) и [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) будут игнорироваться между абзацами одного и того же стиля.

 **Remarks:** 

Этот параметр действует только при применении к стилю абзаца. Если применить его непосредственно к абзацу, он не оказывает влияния.

 **Examples:** 

Показывает, как применить отсутствие интервала между абзацами с одинаковым стилем.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
 // no spacing between paragraphs with the same style, which will group similar paragraphs.
 // Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
 // to evenly apply spacing to every paragraph.
 builder.getParagraphFormat().setNoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Quote"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getOutlineLevel() {#getOutlineLevel}
```
public int getOutlineLevel()
```


Указывает уровень структуры абзаца в документе.

 **Examples:** 

Показывает, как настроить уровни структуры абзаца для создания сворачиваемого текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```

**Returns:**
int - Соответствующее значение int. Возвращаемое значение является одним из констант [OutlineLevel](../../com.aspose.words/outlinelevel/).
### getPageBreakBefore() {#getPageBreakBefore}
```
public boolean getPageBreakBefore()
```


Истина, если перед абзацем принудительно вставлен разрыв страницы.

 **Examples:** 

Показывает, как создавать абзацы с разрывом страницы в начале.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set this flag to "true" to apply a page break to each paragraph's beginning
 // that the document builder will create under this ParagraphFormat configuration.
 // The first paragraph will not receive a page break.
 // Leave this flag as "false" to start each new paragraph on the same page
 // as the previous, provided there is sufficient space.
 builder.getParagraphFormat().setPageBreakBefore(pageBreakBefore);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 LayoutCollector layoutCollector = new LayoutCollector(doc);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 if (pageBreakBefore) {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(2, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 } else {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.PageBreakBefore.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getRightIndent() {#getRightIndent}
```
public double getRightIndent()
```


Возвращает значение (в пунктах), представляющее правый отступ абзаца.

 **Examples:** 

Показывает, как настроить форматирование абзаца для создания текста со смещением от центра.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Returns:**
double - Значение (в пунктах), представляющее правый отступ для абзаца.
### getShading() {#getShading}
```
public Shading getShading()
```


Возвращает объект [Shading](../../com.aspose.words/shading/), который относится к форматированию затенения абзаца.

 **Examples:** 

Показывает, как оформить текст границами и затенением.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the paragraph.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Указывает, следует ли текущему абзацу использовать настройки сеточных линий документа на страницу при размещении содержимого в абзаце.

 **Examples:** 

Показывает, как задать ограничение количества строк, которое может быть на каждой странице.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Возвращает количество интервала (в пунктах) после абзаца.

**Returns:**
double - Количество интервала (в пунктах) после абзаца.
### getSpaceAfterAuto() {#getSpaceAfterAuto}
```
public boolean getSpaceAfterAuto()
```


Истина, если количество интервала после абзаца задаётся автоматически.

 **Remarks:** 

Когда установлено в true, переопределяет действие [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

Когда вы устанавливаете параметры Space Before и Space After абзаца в Auto, Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Показывает, как задать автоматический интервал абзаца.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSpaceBefore() {#getSpaceBefore}
```
public double getSpaceBefore()
```


Возвращает количество интервала (в пунктах) перед абзацем.

**Returns:**
double - Количество интервала (в пунктах) перед абзацем.
### getSpaceBeforeAuto() {#getSpaceBeforeAuto}
```
public boolean getSpaceBeforeAuto()
```


Истина, если количество интервала перед абзацем задаётся автоматически.

 **Remarks:** 

Когда установлено в true, переопределяет действие [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

Когда вы устанавливаете параметры Space Before и Space After абзаца в Auto, Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Показывает, как задать автоматический интервал абзаца.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Возвращает стиль абзаца, применённый к этому форматированию.

 **Examples:** 

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The paragraph style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Возвращает независимый от локали идентификатор стиля абзаца, применённый к этому форматированию.

 **Examples:** 

Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Returns:**
int - Независимый от локали идентификатор стиля абзаца, применённого к этому форматированию. Возвращаемое значение является одним из констант [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Возвращает название стиля абзаца, применённого к этому форматированию.

 **Examples:** 

Показывает, как вручную создать документ Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
java.lang.String - Имя стиля абзаца, применённого к этому форматированию.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens}
```
public boolean getSuppressAutoHyphens()
```


Указывает, следует ли освобождать текущий абзац от любой переноски, применяемой в настройках документа.

 **Examples:** 

Показывает, как подавить переносы в абзаце.

```

 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary.
 // When we save this document to a fixed page save format, its text will have hyphenation.
 Document doc = new Document(getMyDir() + "German text.docx");

 // We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
 // for a specific paragraph while keeping it enabled for the rest of the document.
 // The default value for this property is "false",
 // which means every paragraph by default uses hyphenation if any is available.
 doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().setSuppressAutoHyphens(suppressAutoHyphens);

 doc.save(getArtifactsDir() + "ParagraphFormat.SuppressHyphens.pdf");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSuppressLineNumbers() {#getSuppressLineNumbers}
```
public boolean getSuppressLineNumbers()
```


Указывает, следует ли освобождать строки текущего абзаца от нумерации строк, применяемой в родительском разделе.

 **Examples:** 

Показывает, как включить нумерацию строк для раздела.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getTabStops() {#getTabStops}
```
public TabStopCollection getTabStops()
```


Возвращает коллекцию пользовательских табуляций, определённых для этого объекта.

 **Examples:** 

Показывает, как изменить позицию правой табуляции в абзацах, связанных с оглавлением (TOC).

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
[TabStopCollection](../../com.aspose.words/tabstopcollection/) - The collection of custom tab stops defined for this object.
### getWidowControl() {#getWidowControl}
```
public boolean getWidowControl()
```


Истина, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца.

 **Examples:** 

Показывает, как включить контроль висячих/сиротских строк для абзаца.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // When we write the text that does not fit onto one page, one line may spill over onto the next page.
 // The single line that ends up on the next page is called an "Orphan",
 // and the previous line where the orphan broke off is called a "Widow".
 // We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
 // If we wish to preserve our document's dimensions, we can set this flag to "true"
 // to push widows onto the same page as their respective orphans.
 // Leave this flag as "false" will leave widow/orphan pairs in text.
 // Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
 // (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
 builder.getParagraphFormat().setWidowControl(widowControl);

 // Insert text that produces an orphan and a widow.
 builder.getFont().setSize(68.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "ParagraphFormat.WidowControl.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getWordWrap() {#getWordWrap}
```
public boolean getWordWrap()
```


Если это свойство установлено в false, латинский текст посередине слова может переноситься в текущем абзаце. В противном случае латинский текст переносится целыми словами.

 **Examples:** 

Показывает, как задать специальные свойства для азиатской типографии.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Истина, когда стиль абзаца является одним из встроенных стилей заголовков.

 **Examples:** 

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохранённого PDF‑документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.PDF);

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
 // The last two headings we have inserted above will not appear.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


Истина, когда абзац является элементом маркированного или нумерованного списка.

 **Examples:** 

Показывает, как вложить список в другой список.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями текста восточноазиатского языка в текущем абзаце.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами латинского текста и регионами текста Восточной Азии в текущем абзаце. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями текста восточноазиатского языка в текущем абзаце.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами чисел и регионами текста Восточной Азии в текущем абзаце. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Устанавливает выравнивание текста для абзаца.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

Показывает, как вручную создать документ Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Выравнивание текста для абзаца. Значение должно быть одним из констант [ParagraphAlignment](../../com.aspose.words/paragraphalignment/). |

### setBaselineAlignment(int value) {#setBaselineAlignment-int}
```
public void setBaselineAlignment(int value)
```


Устанавливает вертикальное положение шрифтов в строке.

 **Examples:** 

Показывает, как установить вертикальное положение шрифтов в строке.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Вертикальное положение шрифтов в строке. Значение должно быть одним из констант [BaselineAlignment](../../com.aspose.words/baselinealignment/). |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Устанавливает, является ли этот абзац направленным справа налево.

 **Remarks:** 

Когда  true , элементы и другие встроенные объекты в этом абзаце размещаются справа налево.

 **Examples:** 

Показывает, как создавать списки, совместимые с языками справа налево, с помощью полей BIDIOUTLINE.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
 // but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
 // The following field will display ".1", the RTL equivalent of list number "1.".
 FieldBidiOutline field = (FieldBidiOutline) builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 Assert.assertEquals(" BIDIOUTLINE ", field.getFieldCode());

 // Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 // Set the horizontal text alignment for every paragraph in the document to RTL.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().setBidi(true);
 }

 // If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
 // Otherwise, they will display "###".
 doc.save(getArtifactsDir() + "Field.BIDIOUTLINE.docx");
 
```

Показывает, как определить направление текста в простом документе.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли это абзацем справа налево. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |
| значение | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double}
```
public void setCharacterUnitFirstLineIndent(double value)
```


Устанавливает значение (в символах) для первой строки или висячего отступа.

Используйте положительные значения для установки отступа первой строки и отрицательные значения для установки висячего отступа.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение (в символах) для первой строки или висячего отступа. |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double}
```
public void setCharacterUnitLeftIndent(double value)
```


Устанавливает значение левого отступа (в символах) для указанных абзацев.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение левого отступа (в символах) для указанных абзацев. |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double}
```
public void setCharacterUnitRightIndent(double value)
```


Устанавливает значение правого отступа (в символах) для указанных абзацев.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение правого отступа (в символах) для указанных абзацев. |

### setDropCapPosition(int value) {#setDropCapPosition-int}
```
public void setDropCapPosition(int value)
```


Устанавливает позицию текста с инициалом.

 **Examples:** 

Показывает, как вложить список в другой список.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Позиция текста с броской буквой. Значение должно быть одним из констант [DropCapPosition](../../com.aspose.words/dropcapposition/). |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean}
```
public void setFarEastLineBreakControl(boolean value)
```


Устанавливает флаг, указывающий, применяются ли правила переноса строк восточноазиатского текста к текущему абзацу.

 **Examples:** 

Показывает, как задать специальные свойства для азиатской типографии.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, применяются ли правила переноса строк Восточной Азии к текущему абзацу. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double}
```
public void setFirstLineIndent(double value)
```


Устанавливает значение (в пунктах) для первой строки или висячего отступа.

Используйте положительные значения для установки отступа первой строки и отрицательные значения для установки висячего отступа.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение (в пунктах) для первой строки или висячего отступа. |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean}
```
public void setHangingPunctuation(boolean value)
```


Устанавливает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

 **Examples:** 

Показывает, как задать специальные свойства для азиатской типографии.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean}
```
public void setKeepTogether(boolean value)
```


Истина, если все строки в абзаце должны оставаться на одной странице.

 **Examples:** 

Показывает, как вставить абзац в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean}
```
public void setKeepWithNext(boolean value)
```


Истина, если абзац должен оставаться на той же странице, что и следующий за ним абзац.

 **Examples:** 

Показывает, как установить таблицу так, чтобы она оставалась вместе на одной странице.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Устанавливает значение (в пунктах), представляющее левый отступ абзаца.

 **Examples:** 

Показывает, как настроить форматирование абзаца для создания текста со смещением от центра.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение (в пунктах), представляющее левый отступ абзаца. |

### setLineSpacing(double value) {#setLineSpacing-double}
```
public void setLineSpacing(double value)
```


Устанавливает межстрочный интервал (в пунктах) для абзаца.

 **Remarks:** 

Когда свойство [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) установлено в [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST), межстрочный интервал может быть больше или равен, но никогда не меньше указанного значения [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

Когда свойство [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) установлено в [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY), межстрочный интервал никогда не меняется от указанного значения [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), даже если в абзаце используется более крупный шрифт.

 **Examples:** 

Показывает, как работать с межстрочным интервалом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Межстрочный интервал (в пунктах) для абзаца. |

### setLineSpacingRule(int value) {#setLineSpacingRule-int}
```
public void setLineSpacingRule(int value)
```


Устанавливает межстрочный интервал для абзаца.

 **Examples:** 

Показывает, как работать с межстрочным интервалом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Межстрочный интервал для абзаца. Значение должно быть одним из констант [LineSpacingRule](../../com.aspose.words/linespacingrule/). |

### setLineUnitAfter(double value) {#setLineUnitAfter-double}
```
public void setLineUnitAfter(double value)
```


Устанавливает величину интервала (в сеточных линиях) после абзацев.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Количество интервала (в сеточных линиях) после абзацев. |

### setLineUnitBefore(double value) {#setLineUnitBefore-double}
```
public void setLineUnitBefore(double value)
```


Устанавливает величину интервала (в сеточных линиях) перед абзацами.

 **Examples:** 

Показывает, как изменить интервалы абзаца и отступы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Количество интервала (в сеточных линиях) перед абзацами. |

### setLinesToDrop(int value) {#setLinesToDrop-int}
```
public void setLinesToDrop(int value)
```


Устанавливает количество строк текста абзаца, используемых для расчёта высоты инициалов.

 **Examples:** 

Показывает, как задать размер буквицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
 // which will turn it into a large capital letter that will decorate the next paragraph.
 // Give this property a value of 4 to give the drop cap the height of four text lines.
 builder.getParagraphFormat().setLinesToDrop(4);
 builder.writeln("H");

 // Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
 // The text in this paragraph will wrap around the drop cap.
 builder.getParagraphFormat().setLinesToDrop(0);
 builder.writeln("ello world!");

 doc.save(getArtifactsDir() + "ParagraphFormat.LinesToDrop.odt");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Количество строк текста абзаца, используемых для расчёта высоты броской буквы. |

### setMirrorIndents(boolean value) {#setMirrorIndents-boolean}
```
public void setMirrorIndents(boolean value)
```


Устанавливает флаг, указывающий, одинаковой ли ширины левый и правый отступы.

 **Examples:** 

Показывает, как сделать одинаковыми отступы слева и справа.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, одинаковой ли ширины левый и правый отступы. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


Когда true, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) и [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) будут игнорироваться между абзацами одного и того же стиля.

 **Remarks:** 

Этот параметр действует только при применении к стилю абзаца. Если применить его непосредственно к абзацу, он не оказывает влияния.

 **Examples:** 

Показывает, как применить отсутствие интервала между абзацами с одинаковым стилем.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
 // no spacing between paragraphs with the same style, which will group similar paragraphs.
 // Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
 // to evenly apply spacing to every paragraph.
 builder.getParagraphFormat().setNoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Quote"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setOutlineLevel(int value) {#setOutlineLevel-int}
```
public void setOutlineLevel(int value)
```


Указывает уровень структуры абзаца в документе.

 **Examples:** 

Показывает, как настроить уровни структуры абзаца для создания сворачиваемого текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одним из констант [OutlineLevel](../../com.aspose.words/outlinelevel/). |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean}
```
public void setPageBreakBefore(boolean value)
```


Истина, если перед абзацем принудительно вставлен разрыв страницы.

 **Examples:** 

Показывает, как создавать абзацы с разрывом страницы в начале.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set this flag to "true" to apply a page break to each paragraph's beginning
 // that the document builder will create under this ParagraphFormat configuration.
 // The first paragraph will not receive a page break.
 // Leave this flag as "false" to start each new paragraph on the same page
 // as the previous, provided there is sufficient space.
 builder.getParagraphFormat().setPageBreakBefore(pageBreakBefore);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 LayoutCollector layoutCollector = new LayoutCollector(doc);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 if (pageBreakBefore) {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(2, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 } else {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.PageBreakBefore.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setRightIndent(double value) {#setRightIndent-double}
```
public void setRightIndent(double value)
```


Устанавливает значение (в пунктах), представляющее правый отступ абзаца.

 **Examples:** 

Показывает, как настроить форматирование абзаца для создания текста со смещением от центра.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение (в пунктах), представляющее правый отступ абзаца. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Указывает, следует ли текущему абзацу использовать настройки сеточных линий документа на страницу при размещении содержимого в абзаце.

 **Examples:** 

Показывает, как задать ограничение количества строк, которое может быть на каждой странице.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Устанавливает величину интервала (в пунктах) после абзаца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Количество интервала (в пунктах) после абзаца. |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean}
```
public void setSpaceAfterAuto(boolean value)
```


Истина, если количество интервала после абзаца задаётся автоматически.

 **Remarks:** 

Когда установлено в true, переопределяет действие [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

Когда вы устанавливаете параметры Space Before и Space After абзаца в Auto, Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Показывает, как задать автоматический интервал абзаца.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSpaceBefore(double value) {#setSpaceBefore-double}
```
public void setSpaceBefore(double value)
```


Устанавливает величину отступа (в пунктах) перед абзацем.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Количество интервала (в пунктах) перед абзацем. |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean}
```
public void setSpaceBeforeAuto(boolean value)
```


Истина, если количество интервала перед абзацем задаётся автоматически.

 **Remarks:** 

Когда установлено в true, переопределяет действие [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

Когда вы устанавливаете параметры Space Before и Space After абзаца в Auto, Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Показывает, как задать автоматический интервал абзаца.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Устанавливает стиль абзаца, применяемый к этому форматированию.

 **Examples:** 

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | Стиль абзаца, применяемый к этому форматированию. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Устанавливает независимый от локали идентификатор стиля абзаца, применяемый к этому форматированию.

 **Examples:** 

Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Независимый от локали идентификатор стиля абзаца, применяемого к этому форматированию. Значение должно быть одним из констант [StyleIdentifier](../../com.aspose.words/styleidentifier/). |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Устанавливает имя стиля абзаца, применяемого к этому форматированию.

 **Examples:** 

Показывает, как вручную создать документ Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя стиля абзаца, применяемого к этому форматированию. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean}
```
public void setSuppressAutoHyphens(boolean value)
```


Указывает, следует ли освобождать текущий абзац от любой переноски, применяемой в настройках документа.

 **Examples:** 

Показывает, как подавить переносы в абзаце.

```

 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary.
 // When we save this document to a fixed page save format, its text will have hyphenation.
 Document doc = new Document(getMyDir() + "German text.docx");

 // We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
 // for a specific paragraph while keeping it enabled for the rest of the document.
 // The default value for this property is "false",
 // which means every paragraph by default uses hyphenation if any is available.
 doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().setSuppressAutoHyphens(suppressAutoHyphens);

 doc.save(getArtifactsDir() + "ParagraphFormat.SuppressHyphens.pdf");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean}
```
public void setSuppressLineNumbers(boolean value)
```


Указывает, следует ли освобождать строки текущего абзаца от нумерации строк, применяемой в родительском разделе.

 **Examples:** 

Показывает, как включить нумерацию строк для раздела.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setWidowControl(boolean value) {#setWidowControl-boolean}
```
public void setWidowControl(boolean value)
```


Истина, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца.

 **Examples:** 

Показывает, как включить контроль висячих/сиротских строк для абзаца.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // When we write the text that does not fit onto one page, one line may spill over onto the next page.
 // The single line that ends up on the next page is called an "Orphan",
 // and the previous line where the orphan broke off is called a "Widow".
 // We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
 // If we wish to preserve our document's dimensions, we can set this flag to "true"
 // to push widows onto the same page as their respective orphans.
 // Leave this flag as "false" will leave widow/orphan pairs in text.
 // Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
 // (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
 builder.getParagraphFormat().setWidowControl(widowControl);

 // Insert text that produces an orphan and a widow.
 builder.getFont().setSize(68.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "ParagraphFormat.WidowControl.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setWordWrap(boolean value) {#setWordWrap-boolean}
```
public void setWordWrap(boolean value)
```


Если это свойство установлено в false, латинский текст посередине слова может переноситься в текущем абзаце. В противном случае латинский текст переносится целыми словами.

 **Examples:** 

Показывает, как задать специальные свойства для азиатской типографии.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

