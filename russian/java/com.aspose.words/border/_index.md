---
title: "Border"
linktitle: "Border"
second_title: "Aspose.Words для Java"
description: "Представляет границу объекта в Java."
type: docs
weight: 46
url: /ru/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Представляет границу объекта.

Чтобы узнать больше, посетите статью документации [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Границы могут применяться к различным элементам документа, включая абзац, последовательность текста внутри абзаца или ячейку таблицы.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

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


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Сбрасывает свойства границы к значениям по умолчанию. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Определяет, равна ли указанная граница по значению текущей границе. |
| [equals(Object obj)](#equals-java.lang.Object) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getColor()](#getColor) | Получает цвет границы. |
| [getDistanceFromText()](#getDistanceFromText) | Получает расстояние границы от текста или от края страницы в пунктах. |
| [getLineStyle()](#getLineStyle) | Получает стиль границы. |
| [getLineWidth()](#getLineWidth) | Получает ширину границы в пунктах. |
| [getShadow()](#getShadow) | Получает значение, указывающее, имеет ли граница тень. |
| [getThemeColor()](#getThemeColor) | Получает цвет темы в применяемой цветовой схеме, связанной с этим объектом Border. |
| [getTintAndShade()](#getTintAndShade) | Получает двойное значение, которое осветляет или затемняет цвет. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Возвращает true, если [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) не является [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает цвет границы. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Устанавливает расстояние границы от текста или от края страницы в пунктах. |
| [setLineStyle(int value)](#setLineStyle-int) | Устанавливает стиль границы. |
| [setLineWidth(double value)](#setLineWidth-double) | Устанавливает ширину границы в пунктах. |
| [setShadow(boolean value)](#setShadow-boolean) | Устанавливает значение, указывающее, имеет ли граница тень. |
| [setThemeColor(int value)](#setThemeColor-int) | Устанавливает цвет темы в применяемой цветовой схеме, связанной с этим объектом Border. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Устанавливает двойное значение, которое осветляет или затемняет цвет. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Сбрасывает свойства границы к значениям по умолчанию.

 **Remarks:** 

Когда свойства границы сбрасываются к значениям по умолчанию, граница становится невидимой.

 **Examples:** 

Показывает, как удалить границы из абзаца.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

### equals(Border rhs) {#equals-com.aspose.words.Border}
```
public boolean equals(Border rhs)
```


Определяет, равна ли указанная граница по значению текущей границе.

 **Examples:** 

Показывает, как коллекции границ могут делить элементы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

 **Examples:** 

Показывает, как коллекции границ могут делить элементы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Получает цвет границы.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
java.awt.Color - Цвет границы.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Получает расстояние границы от текста или от края страницы в пунктах.

 **Remarks:** 

Не оказывает влияния и будет автоматически сброшено до нуля для границ ячеек таблицы.

 **Examples:** 

Показывает, как создать широкую синюю полосу‑границу в верхней части первой страницы.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
double — расстояние границы от текста или от края страницы в пунктах.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Получает стиль границы.

 **Remarks:** 

Если установить стиль линии в none, ширина линии автоматически изменяется на ноль.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
int - Стиль границы. Возвращаемое значение является одним из констант [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Получает ширину границы в пунктах.

 **Remarks:** 

Если установить ширину линии больше нуля, когда стиль линии — none, стиль линии автоматически меняется на одинарную линию.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
double - Ширина границы в пунктах.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Получает значение, указывающее, имеет ли граница тень.

 **Remarks:** 

В Microsoft Word, чтобы у границы была тень, границы со всех четырёх сторон (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета, и у всех должна быть установлена свойство Shadow в true.

 **Examples:** 

Показывает, как создать зеленую волнистую границу страницы с тенью.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
boolean - Значение, указывающее, имеет ли граница тень.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Получает цвет темы в применяемой цветовой схеме, связанной с этим объектом Border.

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
int — цвет темы в применяемой цветовой схеме, связанной с этим объектом Border. Возвращаемое значение — один из констант [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Получает двойное значение, которое осветляет или затемняет цвет.

**Returns:**
double — двойное значение, которое осветляет или затемняет цвет.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Возвращает true, если [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) не является [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

 **Examples:** 

Показывает, как удалить границы из абзаца.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

**Returns:**
boolean — true, если [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) не является [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Устанавливает цвет границы.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет границы. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Устанавливает расстояние границы от текста или от края страницы в пунктах.

 **Remarks:** 

Не оказывает влияния и будет автоматически сброшено до нуля для границ ячеек таблицы.

 **Examples:** 

Показывает, как создать широкую синюю полосу‑границу в верхней части первой страницы.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Расстояние границы от текста или от края страницы в пунктах. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Устанавливает стиль границы.

 **Remarks:** 

Если установить стиль линии в none, ширина линии автоматически изменяется на ноль.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Стиль границы. Значение должно быть одним из констант [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Устанавливает ширину границы в пунктах.

 **Remarks:** 

Если установить ширину линии больше нуля, когда стиль линии — none, стиль линии автоматически меняется на одинарную линию.

 **Examples:** 

Показывает, как вставить строку, окружённую границей, в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Ширина границы в пунктах. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Устанавливает значение, указывающее, имеет ли граница тень.

 **Remarks:** 

В Microsoft Word, чтобы у границы была тень, границы со всех четырёх сторон (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета, и у всех должна быть установлена свойство Shadow в true.

 **Examples:** 

Показывает, как создать зеленую волнистую границу страницы с тенью.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, имеет ли граница тень. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Устанавливает цвет темы в применяемой цветовой схеме, связанной с этим объектом Border.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Цвет темы в применяемой цветовой схеме, связанной с этим объектом Border. Значение должно быть одной из констант [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Устанавливает двойное значение, которое осветляет или затемняет цвет.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Двойное значение, которое осветляет или затемняет цвет. |

