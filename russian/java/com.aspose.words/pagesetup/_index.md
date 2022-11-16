---
title: PageSetup
second_title: Справочник по API Aspose.Words для Java
description: Представляет свойства настройки страницы раздела.
type: docs
weight: 440
url: /ru/java/com.aspose.words/pagesetup/
---

**Наследование:**
java.lang.Object
```
public class PageSetup
```

Представляет свойства настройки страницы раздела.

 Чтобы узнать больше, посетите**Working with Sections** документальная статья.

**PageSetup** объект содержит все атрибуты настройки страницы раздела (левое поле, нижнее поле, размер бумаги и т. д.) в качестве свойств.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Сбрасывает настройки страницы на размер бумаги, поля и ориентацию по умолчанию. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getBidi()](#getBidi--) | Указывает, что этот раздел содержит двунаправленный текст (сложные сценарии). |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront--) | Указывает, где расположена граница страницы относительно пересекающихся текстов и объектов. |
| [getBorderAppliesTo()](#getBorderAppliesTo--) | Указывает, на каких страницах печатается граница страницы. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom--) | Получает значение, указывающее, измеряется ли заданная граница страницы от края страницы или от окружающего ее текста. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter--) | Указывает, включает ли граница страницы нижний колонтитул или исключает его. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader--) | Указывает, включает ли граница страницы заголовок или исключает его. |
| [getBorders()](#getBorders--) | Получает коллекцию границ страницы. |
| [getBottomMargin()](#getBottomMargin--) | Получает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста. |
| [getChapterPageSeparator()](#getChapterPageSeparator--) | Получает символ-разделитель, который появляется между номером главы и номером страницы. |
| [getCharactersPerLine()](#getCharactersPerLine--) | Получает количество символов в строке в сетке документа. |
| [getClass()](#getClass--) |  |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter--) | **True** если на первой странице используется другой верхний или нижний колонтитул. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getEndnoteOptions()](#getEndnoteOptions--) | Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом разделе. |
| [getFirstPageTray()](#getFirstPageTray--) | Получает лоток для бумаги (лоток), используемый для первой страницы раздела. |
| [getFooterDistance()](#getFooterDistance--) | Получает расстояние (в пунктах) между нижним колонтитулом и нижней частью страницы. |
| [getFootnoteOptions()](#getFootnoteOptions--) | Предоставляет параметры, управляющие нумерацией и расположением сносок в этом разделе. |
| [getGutter()](#getGutter--) | Получает количество дополнительного пространства, добавляемого к полю для переплета документа. |
| [getHeaderDistance()](#getHeaderDistance--) | Получает расстояние (в пунктах) между заголовком и верхней частью страницы. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter--) | Получает стиль уровня заголовков, который применяется к заголовкам глав в документе. |
| [getLayoutMode()](#getLayoutMode--) | Получает режим макета этого раздела. |
| [getLeftMargin()](#getLeftMargin--) | Получает расстояние (в пунктах) между левым краем страницы и левой границей основного текста. |
| [getLineNumberCountBy()](#getLineNumberCountBy--) | Получает числовое приращение для номеров строк. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText--) | Получает расстояние между правым краем номеров строк и левым краем документа. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode--) | Получает способ выполнения нумерации строк, т. е. начинается ли она заново в начале новой страницы или раздела или выполняется непрерывно. |
| [getLineStartingNumber()](#getLineStartingNumber--) | Получает номер начальной строки. |
| [getLinesPerPage()](#getLinesPerPage--) | Получает количество строк на странице в сетке документа. |
| [getMultiplePages()](#getMultiplePages--) | Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было переплести в виде буклета. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter--) | **True** если документ имеет разные верхние и нижние колонтитулы для четных и нечетных страниц. |
| [getOrientation()](#getOrientation--) | Получает ориентацию страницы. |
| [getOtherPagesTray()](#getOtherPagesTray--) | Получает лоток для бумаги (лоток), который будет использоваться для всех страниц раздела, кроме первой. |
| [getPageHeight()](#getPageHeight--) | Получает высоту страницы в пунктах. |
| [getPageNumberStyle()](#getPageNumberStyle--) | Получает формат номера страницы. |
| [getPageStartingNumber()](#getPageStartingNumber--) | Получает номер начальной страницы раздела. |
| [getPageWidth()](#getPageWidth--) | Получает ширину страницы в пунктах. |
| [getPaperSize()](#getPaperSize--) | Получает размер бумаги. |
| [getRestartPageNumbering()](#getRestartPageNumbering--) | **True** если нумерация страниц возобновляется с начала раздела. |
| [getRightMargin()](#getRightMargin--) | Получает расстояние (в пунктах) между правым краем страницы и правой границей основного текста. |
| [getRtlGutter()](#getRtlGutter--) | Получает, использует ли Microsoft Word промежутки для раздела на основе языка с письмом справа налево или языка с письмом слева направо. |
| [getSectionStart()](#getSectionStart--) | Получает тип разрыва раздела для указанного объекта. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet--) | Получает количество страниц, которые должны быть включены в каждый буклет. |
| [getSuppressEndnotes()](#getSuppressEndnotes--) | **True** если концевые сноски печатаются в конце следующего раздела, который не подавляет концевые сноски. |
| [getTextColumns()](#getTextColumns--) | Возвращает коллекцию, представляющую набор текстовых столбцов. |
| [getTextOrientation()](#getTextOrientation--) |  Позволяет указать[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) на всю страницу. |
| [getTopMargin()](#getTopMargin--) | Получает расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Получает вертикальное выравнивание текста на каждой странице документа или раздела. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBidi(boolean value)](#setBidi-boolean-) | Указывает, что этот раздел содержит двунаправленный текст (сложные сценарии). |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean-) | Указывает, где расположена граница страницы относительно пересекающихся текстов и объектов. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int-) | Указывает, на каких страницах печатается граница страницы. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int-) | Задает значение, указывающее, измеряется ли указанная граница страницы от края страницы или от окружающего ее текста. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean-) | Указывает, включает ли граница страницы нижний колонтитул или исключает его. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean-) | Указывает, включает ли граница страницы заголовок или исключает его. |
| [setBottomMargin(double value)](#setBottomMargin-double-) | Устанавливает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int-) | Устанавливает символ-разделитель, который появляется между номером главы и номером страницы. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int-) | Устанавливает количество символов в строке в сетке документа. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean-) | **True** если на первой странице используется другой верхний или нижний колонтитул. |
| [setFirstPageTray(int value)](#setFirstPageTray-int-) | Задает лоток для бумаги (лоток), который будет использоваться для первой страницы раздела. |
| [setFooterDistance(double value)](#setFooterDistance-double-) | Устанавливает расстояние (в пунктах) между нижним колонтитулом и нижней частью страницы. |
| [setGutter(double value)](#setGutter-double-) | Устанавливает количество дополнительного пространства, добавляемого к полю для переплета документа. |
| [setHeaderDistance(double value)](#setHeaderDistance-double-) | Устанавливает расстояние (в пунктах) между заголовком и верхом страницы. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int-) | Задает стиль уровня заголовков, который применяется к заголовкам глав в документе. |
| [setLayoutMode(int value)](#setLayoutMode-int-) | Устанавливает режим макета этого раздела. |
| [setLeftMargin(double value)](#setLeftMargin-double-) | Устанавливает расстояние (в пунктах) между левым краем страницы и левой границей основного текста. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int-) | Устанавливает числовое приращение для номеров строк. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double-) | Устанавливает расстояние между правым краем номеров строк и левым краем документа. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int-) | Устанавливает способ выполнения нумерации строк, то есть начинается ли она сначала в начале новой страницы или раздела или выполняется непрерывно. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int-) | Устанавливает номер начальной строки. |
| [setLinesPerPage(int value)](#setLinesPerPage-int-) | Задает количество строк на странице в сетке документа. |
| [setMultiplePages(int value)](#setMultiplePages-int-) | Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было переплести в виде буклета. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean-) | **True** если документ имеет разные верхние и нижние колонтитулы для четных и нечетных страниц. |
| [setOrientation(int value)](#setOrientation-int-) | Устанавливает ориентацию страницы. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int-) | Задает использование лотка для бумаги (корзины) для всех страниц раздела, кроме первой. |
| [setPageHeight(double value)](#setPageHeight-double-) | Устанавливает высоту страницы в пунктах. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int-) | Устанавливает формат номера страницы. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int-) | Устанавливает номер начальной страницы раздела. |
| [setPageWidth(double value)](#setPageWidth-double-) | Устанавливает ширину страницы в пунктах. |
| [setPaperSize(int value)](#setPaperSize-int-) | Устанавливает размер бумаги. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean-) | **True** если нумерация страниц возобновляется с начала раздела. |
| [setRightMargin(double value)](#setRightMargin-double-) | Задает расстояние (в пунктах) между правым краем страницы и правой границей основного текста. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean-) | Устанавливает, использует ли Microsoft Word промежутки для раздела на основе языка с письмом справа налево или языка с письмом слева направо. |
| [setSectionStart(int value)](#setSectionStart-int-) | Задает тип разрыва раздела для указанного объекта. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int-) | Устанавливает количество страниц, которые должны быть включены в каждый буклет. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean-) | **True** если концевые сноски печатаются в конце следующего раздела, который не подавляет концевые сноски. |
| [setTextOrientation(int value)](#setTextOrientation-int-) |  Позволяет указать[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) на всю страницу. |
| [setTopMargin(double value)](#setTopMargin-double-) | Задает расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Задает вертикальное выравнивание текста на каждой странице документа или раздела. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Сбрасывает настройки страницы на размер бумаги, поля и ориентацию по умолчанию.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Указывает, что этот раздел содержит двунаправленный текст (сложные сценарии).

При значении true столбцы в этом разделе располагаются справа налево.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorderAlwaysInFront() {#getBorderAlwaysInFront--}
```
public boolean getBorderAlwaysInFront()
```


Указывает, где расположена граница страницы относительно пересекающихся текстов и объектов.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorderAppliesTo() {#getBorderAppliesTo--}
```
public int getBorderAppliesTo()
```


Указывает, на каких страницах печатается граница страницы.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto) константы.
### getBorderDistanceFrom() {#getBorderDistanceFrom--}
```
public int getBorderDistanceFrom()
```


Получает значение, указывающее, измеряется ли заданная граница страницы от края страницы или от окружающего ее текста.

**Возвращает:**
 int — значение, указывающее, измеряется ли указанная граница страницы от края страницы или от окружающего ее текста. Возвращаемое значение является одним из[PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom) константы.
### getBorderSurroundsFooter() {#getBorderSurroundsFooter--}
```
public boolean getBorderSurroundsFooter()
```


Указывает, включает ли граница страницы нижний колонтитул или исключает его. Обратите внимание, что изменение этого свойства влияет на все разделы документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorderSurroundsHeader() {#getBorderSurroundsHeader--}
```
public boolean getBorderSurroundsHeader()
```


Указывает, включает ли граница страницы заголовок или исключает его. Обратите внимание, что изменение этого свойства влияет на все разделы документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ страницы.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Коллекция границ страницы.
### getBottomMargin() {#getBottomMargin--}
```
public double getBottomMargin()
```


Получает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста.

**Возвращает:**
double — расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста.
### getChapterPageSeparator() {#getChapterPageSeparator--}
```
public int getChapterPageSeparator()
```


Получает символ-разделитель, который появляется между номером главы и номером страницы.

Прежде чем вы сможете создавать номера страниц, включающие номера глав, к заголовкам документа должен быть применен нумерованный формат структуры.

**Возвращает:**
 int — символ-разделитель, который появляется между номером главы и номером страницы. Возвращаемое значение является одним из[ChapterPageSeparator](../../com.aspose.words/chapterpageseparator) константы.
### getCharactersPerLine() {#getCharactersPerLine--}
```
public int getCharactersPerLine()
```


Получает количество символов в строке в сетке документа.

Минимальное значение свойства равно 1. Максимальное значение зависит от ширины страницы и размера шрифта стиля Normal. Минимальный шаг символов составляет 90 процентов от размера шрифта. Например, максимальное количество символов в строке страницы Letter с полями в один дюйм равно 43.

По умолчанию свойство имеет значение, при котором шаг символов равен размеру шрифта стиля Normal.

**Возвращает:**
int — количество символов в строке в сетке документа.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter--}
```
public boolean getDifferentFirstPageHeaderFooter()
```


**True** если на первой странице используется другой верхний или нижний колонтитул.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом разделе.

**Возвращает:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - соответствующий[EndnoteOptions](../../com.aspose.words/endnoteoptions) ценность.
### getFirstPageTray() {#getFirstPageTray--}
```
public int getFirstPageTray()
```


Получает лоток для бумаги (лоток), используемый для первой страницы раздела. Значение зависит от реализации (принтера).

**Возвращает:**
int — лоток для бумаги (лоток), используемый для первой страницы раздела.
### getFooterDistance() {#getFooterDistance--}
```
public double getFooterDistance()
```


Получает расстояние (в пунктах) между нижним колонтитулом и нижней частью страницы.

**Возвращает:**
double - Расстояние (в пунктах) между нижним колонтитулом и низом страницы.
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


Предоставляет параметры, управляющие нумерацией и расположением сносок в этом разделе.

**Возвращает:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - соответствующий[FootnoteOptions](../../com.aspose.words/footnoteoptions) ценность.
### getGutter() {#getGutter--}
```
public double getGutter()
```


Получает количество дополнительного пространства, добавляемого к полю для переплета документа.

**Возвращает:**
double — количество дополнительного пространства, добавляемого к полю для переплета документа.
### getHeaderDistance() {#getHeaderDistance--}
```
public double getHeaderDistance()
```


Получает расстояние (в пунктах) между заголовком и верхней частью страницы.

**Возвращает:**
double - Расстояние (в пунктах) между заголовком и верхом страницы.
### getHeadingLevelForChapter() {#getHeadingLevelForChapter--}
```
public int getHeadingLevelForChapter()
```


Получает стиль уровня заголовков, который применяется к заголовкам глав в документе.

Может быть числом от 0 до 9. 0 означает отсутствие номера главы, если применяется к номеру страницы.

Прежде чем вы сможете создавать номера страниц, включающие номера глав, к заголовкам документа должен быть применен нумерованный формат структуры.

**Возвращает:**
int — стиль уровня заголовков, применяемый к заголовкам глав в документе.
### getLayoutMode() {#getLayoutMode--}
```
public int getLayoutMode()
```


Получает режим макета этого раздела.

**Возвращает:**
 int - Режим макета этого раздела. Возвращаемое значение является одним из[SectionLayoutMode](../../com.aspose.words/sectionlayoutmode) константы.
### getLeftMargin() {#getLeftMargin--}
```
public double getLeftMargin()
```


Получает расстояние (в пунктах) между левым краем страницы и левой границей основного текста.

**Возвращает:**
double — расстояние (в пунктах) между левым краем страницы и левой границей основного текста.
### getLineNumberCountBy() {#getLineNumberCountBy--}
```
public int getLineNumberCountBy()
```


Получает числовое приращение для номеров строк.

**Возвращает:**
int - числовое приращение для номеров строк.
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText--}
```
public double getLineNumberDistanceFromText()
```


Получает расстояние между правым краем номеров строк и левым краем документа. Установите это свойство равным нулю для автоматического расстояния между номерами строк и текстом документа.

**Возвращает:**
double - Расстояние между правым краем номеров строк и левым краем документа.
### getLineNumberRestartMode() {#getLineNumberRestartMode--}
```
public int getLineNumberRestartMode()
```


Получает способ выполнения нумерации строк, т. е. начинается ли она заново в начале новой страницы или раздела или выполняется непрерывно.

**Возвращает:**
 int - способ нумерации строк, то есть, начинается ли она сначала в начале новой страницы или раздела или выполняется непрерывно. Возвращаемое значение является одним из[LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode) константы.
### getLineStartingNumber() {#getLineStartingNumber--}
```
public int getLineStartingNumber()
```


Получает номер начальной строки.

**Возвращает:**
int - Начальный номер строки.
### getLinesPerPage() {#getLinesPerPage--}
```
public int getLinesPerPage()
```


Получает количество строк на странице в сетке документа.

Минимальное значение свойства равно 1. Максимальное значение зависит от высоты страницы и размера шрифта стиля Normal. Минимальный шаг строки составляет 136 процентов от размера шрифта. Например, максимальное количество строк на странице Letter с полями в один дюйм равно 39.

По умолчанию свойство имеет значение, при котором шаг строки в 1,5 раза больше размера шрифта стиля Normal.

**Возвращает:**
int — количество строк на странице в сетке документа.
### getMultiplePages() {#getMultiplePages--}
```
public int getMultiplePages()
```


Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было переплести в виде буклета.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MultiplePagesType](../../com.aspose.words/multiplepagestype) константы.
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter--}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


**True**если документ имеет разные верхние и нижние колонтитулы для четных и нечетных страниц. Обратите внимание, что изменение этого свойства влияет на все разделы документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOrientation() {#getOrientation--}
```
public int getOrientation()
```


Получает ориентацию страницы.

 изменение**Orientation** свопы[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) а также[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-).

**Возвращает:**
 int - Ориентация страницы. Возвращаемое значение является одним из[Orientation](../../com.aspose.words/orientation) константы.
### getOtherPagesTray() {#getOtherPagesTray--}
```
public int getOtherPagesTray()
```


Получает лоток для бумаги (лоток), который будет использоваться для всех страниц раздела, кроме первой. Значение зависит от реализации (принтера).

**Возвращает:**
int — лоток для бумаги (лоток), который будет использоваться для всех страниц раздела, кроме первой.
### getPageHeight() {#getPageHeight--}
```
public double getPageHeight()
```


Получает высоту страницы в пунктах.

**Возвращает:**
double - Высота страницы в пунктах.
### getPageNumberStyle() {#getPageNumberStyle--}
```
public int getPageNumberStyle()
```


Получает формат номера страницы.

**Возвращает:**
 int - Формат номера страницы. Возвращаемое значение является одним из[NumberStyle](../../com.aspose.words/numberstyle) константы.
### getPageStartingNumber() {#getPageStartingNumber--}
```
public int getPageStartingNumber()
```


 Получает номер начальной страницы раздела.[getRestartPageNumbering()](../../com.aspose.words/pagesetup\#getRestartPageNumbering--) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup\#setRestartPageNumbering-boolean-) свойство, если установлено**false** , переопределит**PageStartingNumber** свойство, чтобы нумерация страниц могла продолжаться с предыдущего раздела.

**Возвращает:**
int — номер начальной страницы раздела.
### getPageWidth() {#getPageWidth--}
```
public double getPageWidth()
```


Получает ширину страницы в пунктах.

**Возвращает:**
double - Ширина страницы в пунктах.
### getPaperSize() {#getPaperSize--}
```
public int getPaperSize()
```


Получает размер бумаги.

 Настройка обновления этого свойства[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) а также[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-) ценности. Установка этого значения на[PaperSize.CUSTOM](../../com.aspose.words/papersize\#CUSTOM) не изменяет существующие значения.

**Возвращает:**
int - Размер бумаги. Возвращаемое значение является одним из[PaperSize](../../com.aspose.words/papersize) константы.
### getRestartPageNumbering() {#getRestartPageNumbering--}
```
public boolean getRestartPageNumbering()
```


**True** если нумерация страниц возобновляется с начала раздела. Если установлено**false** ,**RestartPageNumbering** свойство переопределит[getPageStartingNumber()](../../com.aspose.words/pagesetup\#getPageStartingNumber--) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup\#setPageStartingNumber-int-) свойство, чтобы нумерация страниц могла продолжаться с предыдущего раздела.

**Возвращает:**
boolean - соответствующее логическое значение.
### getRightMargin() {#getRightMargin--}
```
public double getRightMargin()
```


Получает расстояние (в пунктах) между правым краем страницы и правой границей основного текста.

**Возвращает:**
double — расстояние (в пунктах) между правым краем страницы и правой границей основного текста.
### getRtlGutter() {#getRtlGutter--}
```
public boolean getRtlGutter()
```


Получает, использует ли Microsoft Word промежутки для раздела на основе языка с письмом справа налево или языка с письмом слева направо.

**Возвращает:**
boolean — использует ли Microsoft Word промежутки для раздела на основе языка с письмом справа налево или языка с письмом слева направо.
### getSectionStart() {#getSectionStart--}
```
public int getSectionStart()
```


Получает тип разрыва раздела для указанного объекта.

**Возвращает:**
 int - Тип разрыва раздела для указанного объекта. Возвращаемое значение является одним из[SectionStart](../../com.aspose.words/sectionstart) константы.
### getSheetsPerBooklet() {#getSheetsPerBooklet--}
```
public int getSheetsPerBooklet()
```


Получает количество страниц, которые должны быть включены в каждый буклет.

**Возвращает:**
int — количество страниц, которые должны быть включены в каждый буклет.
### getSuppressEndnotes() {#getSuppressEndnotes--}
```
public boolean getSuppressEndnotes()
```


**True** если концевые сноски печатаются в конце следующего раздела, который не подавляет концевые сноски. Подавленные концевые сноски печатаются перед концевыми сносками в этом разделе.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTextColumns() {#getTextColumns--}
```
public TextColumnCollection getTextColumns()
```


Возвращает коллекцию, представляющую набор текстовых столбцов.

**Возвращает:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection) - Коллекция, представляющая набор текстовых столбцов.
### getTextOrientation() {#getTextOrientation--}
```
public int getTextOrientation()
```


 Позволяет указать[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) на всю страницу. Значение по умолчанию[TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation\#HORIZONTAL) Это свойство поддерживается только для родных форматов MS Word DOCX, WML, RTF и DOC.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[TextOrientation](../../com.aspose.words/textorientation) константы.
### getTopMargin() {#getTopMargin--}
```
public double getTopMargin()
```


Получает расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста.

**Возвращает:**
double — расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Получает вертикальное выравнивание текста на каждой странице документа или раздела.

**Возвращает:**
 int — Вертикальное выравнивание текста на каждой странице документа или раздела. Возвращаемое значение является одним из[PageVerticalAlignment](../../com.aspose.words/pageverticalalignment) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Указывает, что этот раздел содержит двунаправленный текст (сложные сценарии).

При значении true столбцы в этом разделе располагаются справа налево.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean-}
```
public void setBorderAlwaysInFront(boolean value)
```


Указывает, где расположена граница страницы относительно пересекающихся текстов и объектов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int-}
```
public void setBorderAppliesTo(int value)
```


Указывает, на каких страницах печатается граница страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto) константы. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int-}
```
public void setBorderDistanceFrom(int value)
```


Задает значение, указывающее, измеряется ли указанная граница страницы от края страницы или от окружающего ее текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, указывающее, измеряется ли заданная граница страницы от края страницы или от окружающего ее текста. Значение должно быть одним из[PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom) константы. |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean-}
```
public void setBorderSurroundsFooter(boolean value)
```


Указывает, включает ли граница страницы нижний колонтитул или исключает его. Обратите внимание, что изменение этого свойства влияет на все разделы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean-}
```
public void setBorderSurroundsHeader(boolean value)
```


Указывает, включает ли граница страницы заголовок или исключает его. Обратите внимание, что изменение этого свойства влияет на все разделы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBottomMargin(double value) {#setBottomMargin-double-}
```
public void setBottomMargin(double value)
```


Устанавливает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста. |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int-}
```
public void setChapterPageSeparator(int value)
```


Устанавливает символ-разделитель, который появляется между номером главы и номером страницы.

Прежде чем вы сможете создавать номера страниц, включающие номера глав, к заголовкам документа должен быть применен нумерованный формат структуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Символ-разделитель, который появляется между номером главы и номером страницы. Значение должно быть одним из[ChapterPageSeparator](../../com.aspose.words/chapterpageseparator) константы. |

### setCharactersPerLine(int value) {#setCharactersPerLine-int-}
```
public void setCharactersPerLine(int value)
```


Устанавливает количество символов в строке в сетке документа.

Минимальное значение свойства равно 1. Максимальное значение зависит от ширины страницы и размера шрифта стиля Normal. Минимальный шаг символов составляет 90 процентов от размера шрифта. Например, максимальное количество символов в строке страницы Letter с полями в один дюйм равно 43.

По умолчанию свойство имеет значение, при котором шаг символов равен размеру шрифта стиля Normal.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество символов в строке в сетке документа. |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean-}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


**True** если на первой странице используется другой верхний или нижний колонтитул.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFirstPageTray(int value) {#setFirstPageTray-int-}
```
public void setFirstPageTray(int value)
```


Задает лоток для бумаги (лоток), который будет использоваться для первой страницы раздела. Значение зависит от реализации (принтера).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Лоток для бумаги (лоток), используемый для первой страницы раздела. |

### setFooterDistance(double value) {#setFooterDistance-double-}
```
public void setFooterDistance(double value)
```


Устанавливает расстояние (в пунктах) между нижним колонтитулом и нижней частью страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между нижним колонтитулом и нижней частью страницы. |

### setGutter(double value) {#setGutter-double-}
```
public void setGutter(double value)
```


Устанавливает количество дополнительного пространства, добавляемого к полю для переплета документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество дополнительного пространства, добавляемого к полю для переплета документа. |

### setHeaderDistance(double value) {#setHeaderDistance-double-}
```
public void setHeaderDistance(double value)
```


Устанавливает расстояние (в пунктах) между заголовком и верхом страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между заголовком и верхней частью страницы. |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int-}
```
public void setHeadingLevelForChapter(int value)
```


Задает стиль уровня заголовков, который применяется к заголовкам глав в документе.

Может быть числом от 0 до 9. 0 означает отсутствие номера главы, если применяется к номеру страницы.

Прежде чем вы сможете создавать номера страниц, включающие номера глав, к заголовкам документа должен быть применен нумерованный формат структуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Стиль уровня заголовков, применяемый к заголовкам глав в документе. |

### setLayoutMode(int value) {#setLayoutMode-int-}
```
public void setLayoutMode(int value)
```


Устанавливает режим макета этого раздела.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Режим макета этого раздела. Значение должно быть одним из[SectionLayoutMode](../../com.aspose.words/sectionlayoutmode) константы. |

### setLeftMargin(double value) {#setLeftMargin-double-}
```
public void setLeftMargin(double value)
```


Устанавливает расстояние (в пунктах) между левым краем страницы и левой границей основного текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между левым краем страницы и левой границей основного текста. |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int-}
```
public void setLineNumberCountBy(int value)
```


Устанавливает числовое приращение для номеров строк.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Числовой приращение для номеров строк. |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double-}
```
public void setLineNumberDistanceFromText(double value)
```


Устанавливает расстояние между правым краем номеров строк и левым краем документа. Установите это свойство равным нулю для автоматического расстояния между номерами строк и текстом документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние между правым краем номеров строк и левым краем документа. |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int-}
```
public void setLineNumberRestartMode(int value)
```


Устанавливает способ выполнения нумерации строк, то есть начинается ли она сначала в начале новой страницы или раздела или выполняется непрерывно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  То, как работает нумерация строк, то есть начинается ли она сначала в начале новой страницы или раздела или выполняется непрерывно. Значение должно быть одним из[LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode) константы. |

### setLineStartingNumber(int value) {#setLineStartingNumber-int-}
```
public void setLineStartingNumber(int value)
```


Устанавливает номер начальной строки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Номер стартовой строки. |

### setLinesPerPage(int value) {#setLinesPerPage-int-}
```
public void setLinesPerPage(int value)
```


Задает количество строк на странице в сетке документа.

Минимальное значение свойства равно 1. Максимальное значение зависит от высоты страницы и размера шрифта стиля Normal. Минимальный шаг строки составляет 136 процентов от размера шрифта. Например, максимальное количество строк на странице Letter с полями в один дюйм равно 39.

По умолчанию свойство имеет значение, при котором шаг строки в 1,5 раза больше размера шрифта стиля Normal.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество строк на странице в сетке документа. |

### setMultiplePages(int value) {#setMultiplePages-int-}
```
public void setMultiplePages(int value)
```


Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было переплести в виде буклета.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MultiplePagesType](../../com.aspose.words/multiplepagestype) константы. |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean-}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


**True**если документ имеет разные верхние и нижние колонтитулы для четных и нечетных страниц. Обратите внимание, что изменение этого свойства влияет на все разделы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOrientation(int value) {#setOrientation-int-}
```
public void setOrientation(int value)
```


Устанавливает ориентацию страницы.

 изменение**Orientation** свопы[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) а также[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Ориентация страницы. Значение должно быть одним из[Orientation](../../com.aspose.words/orientation) константы. |

### setOtherPagesTray(int value) {#setOtherPagesTray-int-}
```
public void setOtherPagesTray(int value)
```


Задает использование лотка для бумаги (корзины) для всех страниц раздела, кроме первой. Значение зависит от реализации (принтера).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Лоток для бумаги (лоток), который будет использоваться для всех страниц раздела, кроме первой. |

### setPageHeight(double value) {#setPageHeight-double-}
```
public void setPageHeight(double value)
```


Устанавливает высоту страницы в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Высота страницы в пунктах. |

### setPageNumberStyle(int value) {#setPageNumberStyle-int-}
```
public void setPageNumberStyle(int value)
```


Устанавливает формат номера страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Формат номера страницы. Значение должно быть одним из[NumberStyle](../../com.aspose.words/numberstyle) константы. |

### setPageStartingNumber(int value) {#setPageStartingNumber-int-}
```
public void setPageStartingNumber(int value)
```


 Устанавливает номер начальной страницы раздела.[getRestartPageNumbering()](../../com.aspose.words/pagesetup\#getRestartPageNumbering--) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup\#setRestartPageNumbering-boolean-) свойство, если установлено**false** , переопределит**PageStartingNumber** свойство, чтобы нумерация страниц могла продолжаться с предыдущего раздела.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Начальный номер страницы раздела. |

### setPageWidth(double value) {#setPageWidth-double-}
```
public void setPageWidth(double value)
```


Устанавливает ширину страницы в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Ширина страницы в пунктах. |

### setPaperSize(int value) {#setPaperSize-int-}
```
public void setPaperSize(int value)
```


Устанавливает размер бумаги.

 Настройка обновления этого свойства[getPageWidth()](../../com.aspose.words/pagesetup\#getPageWidth--) / [setPageWidth(double)](../../com.aspose.words/pagesetup\#setPageWidth-double-) а также[getPageHeight()](../../com.aspose.words/pagesetup\#getPageHeight--) / [setPageHeight(double)](../../com.aspose.words/pagesetup\#setPageHeight-double-) ценности. Установка этого значения на[PaperSize.CUSTOM](../../com.aspose.words/papersize\#CUSTOM) не изменяет существующие значения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Размер бумаги. Значение должно быть одним из[PaperSize](../../com.aspose.words/papersize) константы. |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean-}
```
public void setRestartPageNumbering(boolean value)
```


**True** если нумерация страниц возобновляется с начала раздела. Если установлено**false** ,**RestartPageNumbering** свойство переопределит[getPageStartingNumber()](../../com.aspose.words/pagesetup\#getPageStartingNumber--) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup\#setPageStartingNumber-int-) свойство, чтобы нумерация страниц могла продолжаться с предыдущего раздела.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setRightMargin(double value) {#setRightMargin-double-}
```
public void setRightMargin(double value)
```


Задает расстояние (в пунктах) между правым краем страницы и правой границей основного текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между правым краем страницы и правой границей основного текста. |

### setRtlGutter(boolean value) {#setRtlGutter-boolean-}
```
public void setRtlGutter(boolean value)
```


Устанавливает, использует ли Microsoft Word промежутки для раздела на основе языка с письмом справа налево или языка с письмом слева направо.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Использует ли Microsoft Word промежутки для раздела на основе языка с письмом справа налево или языка с письмом слева направо. |

### setSectionStart(int value) {#setSectionStart-int-}
```
public void setSectionStart(int value)
```


Задает тип разрыва раздела для указанного объекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Тип разрыва раздела для указанного объекта. Значение должно быть одним из[SectionStart](../../com.aspose.words/sectionstart) константы. |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int-}
```
public void setSheetsPerBooklet(int value)
```


Устанавливает количество страниц, которые должны быть включены в каждый буклет.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество страниц, которые должны быть включены в каждый буклет. |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean-}
```
public void setSuppressEndnotes(boolean value)
```


**True** если концевые сноски печатаются в конце следующего раздела, который не подавляет концевые сноски. Подавленные концевые сноски печатаются перед концевыми сносками в этом разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTextOrientation(int value) {#setTextOrientation-int-}
```
public void setTextOrientation(int value)
```


 Позволяет указать[getTextOrientation()](../../com.aspose.words/pagesetup\#getTextOrientation--) / [setTextOrientation(int)](../../com.aspose.words/pagesetup\#setTextOrientation-int-) на всю страницу. Значение по умолчанию[TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation\#HORIZONTAL) Это свойство поддерживается только для родных форматов MS Word DOCX, WML, RTF и DOC.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[TextOrientation](../../com.aspose.words/textorientation) константы. |

### setTopMargin(double value) {#setTopMargin-double-}
```
public void setTopMargin(double value)
```


Задает расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


Задает вертикальное выравнивание текста на каждой странице документа или раздела.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Вертикальное выравнивание текста на каждой странице документа или раздела. Значение должно быть одним из[PageVerticalAlignment](../../com.aspose.words/pageverticalalignment) константы. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
