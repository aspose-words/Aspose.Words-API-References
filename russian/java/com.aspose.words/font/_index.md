---
title: "Font"
linktitle: "Font"
second_title: "Aspose.Words для Java"
description: "Содержит атрибуты шрифта: имя шрифта, размер шрифта, цвет и т.д. для объекта в Java."
type: docs
weight: 319
url: /ru/java/com.aspose.words/font/
---

**Inheritance:**
java.lang.Object
```
public class Font
```

Содержит атрибуты шрифта (название шрифта, размер шрифта, цвет и т.д.) для объекта.

Чтобы узнать больше, посетите статью документации [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Вы не создаёте экземпляры класса [Font](../../com.aspose.words/font/) напрямую. Вы просто используете [Font](../../com.aspose.words/font/) для доступа к свойствам шрифта различных объектов, таких как [Run](../../com.aspose.words/run/), [Paragraph](../../com.aspose.words/paragraph/), [Style](../../com.aspose.words/style/), [DocumentBuilder](../../com.aspose.words/documentbuilder/).

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

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

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


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Сбрасывает форматирование шрифта к значениям по умолчанию. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAllCaps()](#getAllCaps) | True, если шрифт отформатирован заглавными буквами. |
| [getAutoColor()](#getAutoColor) | Возвращает текущий вычисленный цвет текста (чёрный или белый), используемый для 'auto color'. |
| [getBidi()](#getBidi) | Указывает, должны ли содержимое этого фрагмента иметь характеристики справа налево. |
| [getBold()](#getBold) | True, если шрифт оформлен как жирный. |
| [getBoldBi()](#getBoldBi) | True, если текст справа налево отформатирован полужирным. |
| [getBorder()](#getBorder) | Возвращает объект [Border](../../com.aspose.words/border/), который задаёт границу для шрифта. |
| [getColor()](#getColor) | Получает цвет шрифта. |
| [getComplexScript()](#getComplexScript) | Указывает, следует ли рассматривать содержимое этого фрагмента как текст сложного скрипта независимо от их значений Unicode при определении форматирования этого фрагмента. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough) | True, если шрифт отформатирован двойным зачеркиванием. |
| [getEmboss()](#getEmboss) | True, если шрифт отформатирован как рельефный. |
| [getEmphasisMark()](#getEmphasisMark) | Получает знак выделения, примененный к этому форматированию. |
| [getEngrave()](#getEngrave) | True, если шрифт отформатирован как гравированный. |
| [getFill()](#getFill) | Получает формат заполнения для [Font](../../com.aspose.words/font/). |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableBaseForeColor()](#getFillableBaseForeColor) |  |
| [getFillableForeColor()](#getFillableForeColor) |  |
| [getFillableForeThemeColor()](#getFillableForeThemeColor) |  |
| [getFillableForeTintAndShade()](#getFillableForeTintAndShade) |  |
| [getFillableImageBytes()](#getFillableImageBytes) |  |
| [getFillableTransparency()](#getFillableTransparency) |  |
| [getFillableVisible()](#getFillableVisible) |  |
| [getFilledColor()](#getFilledColor) |  |
| [getGradientAngle()](#getGradientAngle) |  |
| [getGradientStops()](#getGradientStops) |  |
| [getGradientStyle()](#getGradientStyle) |  |
| [getGradientVariant()](#getGradientVariant) |  |
| [getHidden()](#getHidden) | True, если шрифт отформатирован как скрытый текст. |
| [getHighlightColor()](#getHighlightColor) | Получает цвет выделения (маркер). |
| [getItalic()](#getItalic) | Истина, если шрифт оформлен курсивом. |
| [getItalicBi()](#getItalicBi) | True, если текст справа налево отформатирован как курсив. |
| [getKerning()](#getKerning) | Получает размер шрифта, при котором начинается кернинг. |
| [getLineSpacing()](#getLineSpacing) | Возвращает межстрочный интервал этого шрифта (в пунктах). |
| [getLocaleId()](#getLocaleId) | Получает идентификатор локали (язык) отформатированных символов. |
| [getLocaleIdBi()](#getLocaleIdBi) | Получает идентификатор локали (язык) отформатированных символов справа налево. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast) | Получает идентификатор локали (язык) отформатированных азиатских символов. |
| [getName()](#getName) | Получает название шрифта. |
| [getNameAscii()](#getNameAscii) | Получает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |
| [getNameBi()](#getNameBi) | Получает имя шрифта в документе с языком справа налево. |
| [getNameFarEast()](#getNameFarEast) | Получает имя восточно-азиатского шрифта. |
| [getNameOther()](#getNameOther) | Получает шрифт, используемый для символов с кодами от 128 до 255. |
| [getNoProofing()](#getNoProofing) | True, когда отформатированные символы не подлежат проверке орфографии. |
| [getNumberSpacing()](#getNumberSpacing) | Получает тип интервала отображаемой цифры. |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOutline()](#getOutline) | True, если шрифт отформатирован как контур. |
| [getPatternType()](#getPatternType) |  |
| [getPosition()](#getPosition) | Получает позицию текста (в пунктах) относительно базовой линии. |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getScaling()](#getScaling) | Получает масштабирование ширины символов в процентах. |
| [getShading()](#getShading) | Возвращает объект [Shading](../../com.aspose.words/shading/), который относится к форматированию затенения для шрифта. |
| [getShadow()](#getShadow) | True, если шрифт отформатирован как с тенью. |
| [getSize()](#getSize) | Получает размер шрифта в пунктах. |
| [getSizeBi()](#getSizeBi) | Получает размер шрифта в пунктах, используемый в документе с направлением справа налево. |
| [getSmallCaps()](#getSmallCaps) | Истина, если шрифт оформлен малыми заглавными буквами. |
| [getSnapToGrid()](#getSnapToGrid) | Указывает, следует ли текущему шрифту использовать настройки количества символов в строке сетки документа при размещении. |
| [getSpacing()](#getSpacing) | Получает интервал (в пунктах) между символами. |
| [getStrikeThrough()](#getStrikeThrough) | Истина, если шрифт оформлен как перечёркнутый. |
| [getStyle()](#getStyle) | Получает стиль символов, примененный к этому форматированию. |
| [getStyleIdentifier()](#getStyleIdentifier) | Получает независимый от локали идентификатор стиля символов, примененный к этому форматированию. |
| [getStyleName()](#getStyleName) | Получает имя стиля символов, примененного к этому форматированию. |
| [getSubscript()](#getSubscript) | Истина, если шрифт отформатирован как нижний индекс. |
| [getSuperscript()](#getSuperscript) | Истина, если шрифт отформатирован как верхний индекс. |
| [getTextEffect()](#getTextEffect) | Получает эффект анимации шрифта. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getThemeColor()](#getThemeColor) | Получает цвет темы в примененной цветовой схеме, связанной с объектом [Font](../../com.aspose.words/font/). |
| [getThemeFont()](#getThemeFont) | Получает шрифт темы в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/). |
| [getThemeFontAscii()](#getThemeFontAscii) | Получает шрифт темы, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/). |
| [getThemeFontBi()](#getThemeFontBi) | Получает шрифт темы в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/) в документе с языком справа налево. |
| [getThemeFontFarEast()](#getThemeFontFarEast) | Получает восточноазиатский шрифт темы в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/). |
| [getThemeFontOther()](#getThemeFontOther) | Получает шрифт темы, используемый для символов с кодами от 128 до 255 в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/). |
| [getTintAndShade()](#getTintAndShade) | Получает двойное значение, которое осветляет или затемняет цвет. |
| [getUnderline()](#getUnderline) | Получает тип подчеркивания, примененного к шрифту. |
| [getUnderlineColor()](#getUnderlineColor) | Получает цвет подчеркивания, примененного к шрифту. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean) | True, если шрифт отформатирован заглавными буквами. |
| [setBidi(boolean value)](#setBidi-boolean) | Указывает, должны ли содержимое этого фрагмента иметь характеристики справа налево. |
| [setBold(boolean value)](#setBold-boolean) | True, если шрифт оформлен как жирный. |
| [setBoldBi(boolean value)](#setBoldBi-boolean) | True, если текст справа налево отформатирован полужирным. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает цвет шрифта. |
| [setComplexScript(boolean value)](#setComplexScript-boolean) | Указывает, следует ли рассматривать содержимое этого фрагмента как текст сложного скрипта независимо от их значений Unicode при определении форматирования этого фрагмента. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean) | True, если шрифт отформатирован двойным зачеркиванием. |
| [setEmboss(boolean value)](#setEmboss-boolean) | True, если шрифт отформатирован как рельефный. |
| [setEmphasisMark(int value)](#setEmphasisMark-int) | Устанавливает знак акцента, применяемый к этому форматированию. |
| [setEngrave(boolean value)](#setEngrave-boolean) | True, если шрифт отформатирован как гравированный. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color) |  |
| [setFillableBackThemeColor(int value)](#setFillableBackThemeColor-int) |  |
| [setFillableBackTintAndShade(double value)](#setFillableBackTintAndShade-double) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color) |  |
| [setFillableForeThemeColor(int value)](#setFillableForeThemeColor-int) |  |
| [setFillableForeTintAndShade(double value)](#setFillableForeTintAndShade-double) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color) |  |
| [setGradientAngle(double value)](#setGradientAngle-double) |  |
| [setHidden(boolean value)](#setHidden-boolean) | True, если шрифт отформатирован как скрытый текст. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color) | Устанавливает цвет выделения (маркировки). |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setItalic(boolean value)](#setItalic-boolean) | Истина, если шрифт оформлен курсивом. |
| [setItalicBi(boolean value)](#setItalicBi-boolean) | True, если текст справа налево отформатирован как курсив. |
| [setKerning(double value)](#setKerning-double) | Устанавливает размер шрифта, при котором начинается кёрнинг. |
| [setLocaleId(int value)](#setLocaleId-int) | Устанавливает идентификатор локали (язык) отформатированных символов. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int) | Устанавливает идентификатор локали (язык) отформатированных символов справа налево. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int) | Устанавливает идентификатор локали (язык) отформатированных азиатских символов. |
| [setName(String value)](#setName-java.lang.String) | Устанавливает имя шрифта. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String) | Устанавливает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |
| [setNameBi(String value)](#setNameBi-java.lang.String) | Устанавливает имя шрифта в документе с языком, пишущимся справа налево. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String) | Устанавливает имя восточноазиатского шрифта. |
| [setNameOther(String value)](#setNameOther-java.lang.String) | Устанавливает шрифт, используемый для символов с кодами от 128 до 255. |
| [setNoProofing(boolean value)](#setNoProofing-boolean) | True, когда отформатированные символы не подлежат проверке орфографии. |
| [setNumberSpacing(int value)](#setNumberSpacing-int) | Устанавливает тип интервала цифры, отображаемой. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setOutline(boolean value)](#setOutline-boolean) | True, если шрифт отформатирован как контур. |
| [setPosition(double value)](#setPosition-double) | Устанавливает позицию текста (в пунктах) относительно базовой линии. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setScaling(int value)](#setScaling-int) | Устанавливает масштабирование ширины символов в процентах. |
| [setShadow(boolean value)](#setShadow-boolean) | True, если шрифт отформатирован как с тенью. |
| [setSize(double value)](#setSize-double) | Устанавливает размер шрифта в пунктах. |
| [setSizeBi(double value)](#setSizeBi-double) | Устанавливает размер шрифта в пунктах, используемый в документе с языком, пишущимся справа налево. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | Истина, если шрифт оформлен малыми заглавными буквами. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Указывает, следует ли текущему шрифту использовать настройки количества символов в строке сетки документа при размещении. |
| [setSpacing(double value)](#setSpacing-double) | Устанавливает интервал (в пунктах) между символами. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | Истина, если шрифт оформлен как перечёркнутый. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Устанавливает стиль символов, применяемый к этому форматированию. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Устанавливает независимый от локали идентификатор стиля символов, применяемый к этому форматированию. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Устанавливает имя стиля символов, применяемого к этому форматированию. |
| [setSubscript(boolean value)](#setSubscript-boolean) | Истина, если шрифт отформатирован как нижний индекс. |
| [setSuperscript(boolean value)](#setSuperscript-boolean) | Истина, если шрифт отформатирован как верхний индекс. |
| [setTextEffect(int value)](#setTextEffect-int) | Устанавливает эффект анимации шрифта. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setThemeColor(int value)](#setThemeColor-int) | Устанавливает цвет темы в примененной цветовой схеме, связанной с этим объектом [Font](../../com.aspose.words/font/). |
| [setThemeFont(int value)](#setThemeFont-int) | Устанавливает шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int) | Устанавливает шрифт темы, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). |
| [setThemeFontBi(int value)](#setThemeFontBi-int) | Устанавливает шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/) в документе с языком, пишущимся справа налево. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int) | Устанавливает восточноазиатский шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). |
| [setThemeFontOther(int value)](#setThemeFontOther-int) | Устанавливает шрифт темы, используемый для символов с кодами от 128 до 255 в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). |
| [setTintAndShade(double value)](#setTintAndShade-double) | Устанавливает двойное значение, которое осветляет или затемняет цвет. |
| [setUnderline(int value)](#setUnderline-int) | Устанавливает тип подчеркивания, применяемый к шрифту. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color) | Устанавливает цвет подчеркивания, применяемого к шрифту. |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Сбрасывает форматирование шрифта к значениям по умолчанию.

 **Remarks:** 

Удаляет все явно указанные форматирования шрифта на объекте, из которого был получен [Font](../../com.aspose.words/font/), чтобы форматирование шрифта наследовалось от соответствующего родителя.

 **Examples:** 

Показывает, как вставить поле гиперссылки.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
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
### getAllCaps() {#getAllCaps}
```
public boolean getAllCaps()
```


True, если шрифт отформатирован заглавными буквами.

 **Examples:** 

Показывает, как отформатировать фрагмент текста для отображения его содержимого заглавными буквами.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getAutoColor() {#getAutoColor}
```
public Color getAutoColor()
```


Возвращает текущий вычисленный цвет текста (черный или белый), используемый для 'автоцвета'. Если цвет не 'авто', то возвращает [getColor()](../../com.aspose.words/font/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/font/\#setColor-java.awt.Color).

 **Remarks:** 

Когда у текста установлен 'автоматический цвет', фактический цвет текста вычисляется автоматически, чтобы он был читаемым на фоне цвета фона. При изменении цвета фона цвет текста в MS Word автоматически переключается на черный или белый, чтобы обеспечить максимальную разборчивость.

 **Examples:** 

Показывает, как улучшить читаемость, автоматически выбирая цвет текста в зависимости от яркости его фона.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If a run's Font object does not specify text color, it will automatically
 // select either black or white depending on the background color's color.
 Assert.assertEquals(0, builder.getFont().getColor().getRGB());

 // The default color for text is black. If the color of the background is dark, black text will be difficult to see.
 // To solve this problem, the AutoColor property will display this text in white.
 builder.getFont().getShading().setBackgroundPatternColor(Color.BLUE);

 builder.writeln("The text color automatically chosen for this run is white.");

 Assert.assertEquals(Color.WHITE.getRGB(), doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getAutoColor().getRGB());

 // If we change the background to a light color, black will be a more
 // suitable text color than white so that the auto color will display it in black.
 builder.getFont().getShading().setBackgroundPatternColor(Color.RED);

 builder.writeln("The text color automatically chosen for this run is black.");

 Assert.assertEquals(Color.BLACK.getRGB(), doc.getFirstSection().getBody().getParagraphs().get(1).getRuns().get(0).getFont().getAutoColor().getRGB());

 doc.save(getArtifactsDir() + "Font.SetFontAutoColor.docx");
 
```

**Returns:**
java.awt.Color - Текущий вычисленный цвет текста (чёрный или белый), используемый для 'auto color'.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Указывает, должны ли содержимое этого фрагмента иметь характеристики справа налево.

 **Remarks:** 

Это свойство, когда включено, не должно использоваться с сильно направленным слева направо текстом. Любое поведение в этом случае не определено. Это свойство, когда выключено, не должно использоваться с сильным текстом справа налево. Любое поведение в этом случае не определено.

Когда содержимое этого фрагмента отображается, все символы должны рассматриваться как символы сложного скрипта для целей форматирования. Это означает, что [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) и соответствующее имя шрифта будут использоваться при рендеринге этого фрагмента.

Также, когда содержимое этого фрагмента отображается, это свойство действует как переопределение справа налево для символов, классифицированных как "слабые типы" и "нейтральные типы".

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getBold() {#getBold}
```
public boolean getBold()
```


True, если шрифт оформлен как жирный.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getBoldBi() {#getBoldBi}
```
public boolean getBoldBi()
```


True, если текст справа налево отформатирован полужирным.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getBorder() {#getBorder}
```
public Border getBorder()
```


Возвращает объект [Border](../../com.aspose.words/border/), который задаёт границу для шрифта.

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
[Border](../../com.aspose.words/border/) - A [Border](../../com.aspose.words/border/) object that specifies border for the font.
### getColor() {#getColor}
```
public Color getColor()
```


Получает цвет шрифта.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как вставить поле гиперссылки.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

**Returns:**
java.awt.Color - Цвет шрифта.
### getComplexScript() {#getComplexScript}
```
public boolean getComplexScript()
```


Указывает, следует ли рассматривать содержимое этого фрагмента как текст сложного скрипта независимо от их значений Unicode при определении форматирования этого фрагмента.

 **Examples:** 

Показывает, как добавить текст, который всегда рассматривается как сложный скрипт.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
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
### getDoubleStrikeThrough() {#getDoubleStrikeThrough}
```
public boolean getDoubleStrikeThrough()
```


True, если шрифт отформатирован двойным зачеркиванием.

 **Examples:** 

Показывает, как добавить зачёркнутую линию к тексту.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getEmboss() {#getEmboss}
```
public boolean getEmboss()
```


True, если шрифт отформатирован как рельефный.

 **Examples:** 

Показывает, как применить эффекты гравировки/тиснения к тексту.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getEmphasisMark() {#getEmphasisMark}
```
public int getEmphasisMark()
```


Получает знак выделения, примененный к этому форматированию.

 **Examples:** 

Показывает, как добавить дополнительный символ, отображаемый над/под глифом.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```

**Returns:**
int - Маркер акцента, применяемый к этому форматированию. Возвращаемое значение является одной из констант [EmphasisMark](../../com.aspose.words/emphasismark/).
### getEngrave() {#getEngrave}
```
public boolean getEngrave()
```


True, если шрифт отформатирован как гравированный.

 **Examples:** 

Показывает, как применить эффекты гравировки/тиснения к тексту.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getFill() {#getFill}
```
public Fill getFill()
```


Получает формат заполнения для [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the [Font](../../com.aspose.words/font/).
### getFillType() {#getFillType}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableBackThemeColor() {#getFillableBackThemeColor}
```
public int getFillableBackThemeColor()
```




**Returns:**
int
### getFillableBackTintAndShade() {#getFillableBackTintAndShade}
```
public double getFillableBackTintAndShade()
```




**Returns:**
double
### getFillableBaseForeColor() {#getFillableBaseForeColor}
```
public Color getFillableBaseForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeThemeColor() {#getFillableForeThemeColor}
```
public int getFillableForeThemeColor()
```




**Returns:**
int
### getFillableForeTintAndShade() {#getFillableForeTintAndShade}
```
public double getFillableForeTintAndShade()
```




**Returns:**
double
### getFillableImageBytes() {#getFillableImageBytes}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilledColor() {#getFilledColor}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/)
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```




**Returns:**
int
### getHidden() {#getHidden}
```
public boolean getHidden()
```


True, если шрифт отформатирован как скрытый текст.

 **Examples:** 

Показывает, как создать фрагмент скрытого текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
 // We will not see or highlight hidden text unless we enable the "Hidden text" option
 // found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
 // and we will be able to access this text programmatically.
 // It is not advised to use this method to hide sensitive information.
 builder.getFont().setHidden(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text will not be visible in the document.");

 doc.save(getArtifactsDir() + "Font.Hidden.docx");
 
```

Показывает, как использовать реализацию DocumentVisitor для удаления всего скрытого содержимого из документа.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getHighlightColor() {#getHighlightColor}
```
public Color getHighlightColor()
```


Получает цвет выделения (маркер).

 **Examples:** 

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
java.awt.Color - Цвет выделения (маркировки).
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Истина, если шрифт оформлен курсивом.

 **Examples:** 

Показывает, как написать курсивный текст с помощью document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getItalicBi() {#getItalicBi}
```
public boolean getItalicBi()
```


True, если текст справа налево отформатирован как курсив.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getKerning() {#getKerning}
```
public double getKerning()
```


Получает размер шрифта, при котором начинается кернинг.

 **Examples:** 

Показывает, как указать размер шрифта, при котором начинается кернинг.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial Black");

 // Set the builder's font size, and minimum size at which kerning will take effect.
 // The font size falls below the kerning threshold, so the run bellow will not have kerning.
 builder.getFont().setSize(18.0);
 builder.getFont().setKerning(24.0);

 builder.writeln("TALLY. (Kerning not applied)");

 // Set the kerning threshold so that the builder's current font size is above it.
 // Any text we add from this point will have kerning applied. The spaces between characters
 // will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
 builder.getFont().setKerning(12.0);

 builder.writeln("TALLY. (Kerning applied)");

 doc.save(getArtifactsDir() + "Font.Kerning.docx");
 
```

**Returns:**
double - Размер шрифта, при котором начинается кернинг.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Возвращает межстрочный интервал этого шрифта (в пунктах).

 **Examples:** 

Показывает, как получить межстрочный интервал шрифта в пунктах.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set different fonts for the DocumentBuilder, and verify their line spacing.
 builder.getFont().setName("Calibri");
 Assert.assertEquals(13.7d, builder.getFont().getLineSpacing(), 1);

 builder.getFont().setName("Times New Roman");
 Assert.assertEquals(13.7d, builder.getFont().getLineSpacing(), 1);
 
```

**Returns:**
double - Межстрочный интервал этого шрифта (в пунктах).
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Получает идентификатор локали (язык) отформатированных символов.

 **Remarks:** 

Список идентификаторов локали см. https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Показывает, как установить локаль текста, который мы добавляем с помощью document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we set the font's locale to English and insert some Russian text,
 // the English locale spell checker will not recognize the text and detect it as a spelling error.
 builder.getFont().setLocaleId(1033);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 // Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
 builder.getFont().setLocaleId(1049);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 doc.save(getArtifactsDir() + "Font.LocaleId.docx");
 
```

**Returns:**
int - Идентификатор локали (язык) отформатированных символов.
### getLocaleIdBi() {#getLocaleIdBi}
```
public int getLocaleIdBi()
```


Получает идентификатор локали (язык) отформатированных символов справа налево.

 **Remarks:** 

Список идентификаторов локали см. https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
int - Идентификатор локали (язык) отформатированных символов справа налево.
### getLocaleIdFarEast() {#getLocaleIdFarEast}
```
public int getLocaleIdFarEast()
```


Получает идентификатор локали (язык) отформатированных азиатских символов.

 **Remarks:** 

Список идентификаторов локали см. https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Показывает, как вставлять и форматировать текст на языке Дальнего Востока.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Returns:**
int - Идентификатор локали (язык) отформатированных азиатских символов.
### getName() {#getName}
```
public String getName()
```


Получает название шрифта.

 **Remarks:** 

При получении возвращает [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

При установке задает [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) и [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) указанным значением.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
java.lang.String - Название шрифта.
### getNameAscii() {#getNameAscii}
```
public String getNameAscii()
```


Получает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127).

 **Examples:** 

Показывает, как Microsoft Word может объединять два разных шрифта в одном фрагменте.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Returns:**
java.lang.String — Шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127).
### getNameBi() {#getNameBi}
```
public String getNameBi()
```


Получает имя шрифта в документе с языком справа налево.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
java.lang.String — Имя шрифта в документе с языком, пишущимся справа налево.
### getNameFarEast() {#getNameFarEast}
```
public String getNameFarEast()
```


Получает имя восточно-азиатского шрифта.

 **Examples:** 

Показывает, как вставлять и форматировать текст на языке Дальнего Востока.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Returns:**
java.lang.String — Имя восточноазиатского шрифта.
### getNameOther() {#getNameOther}
```
public String getNameOther()
```


Получает шрифт, используемый для символов с кодами от 128 до 255.

 **Examples:** 

Показывает, как Microsoft Word может объединять два разных шрифта в одном фрагменте.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Returns:**
java.lang.String — Шрифт, используемый для символов с кодами от 128 до 255.
### getNoProofing() {#getNoProofing}
```
public boolean getNoProofing()
```


True, когда отформатированные символы не подлежат проверке орфографии.

 **Examples:** 

Показывает, как предотвратить проверку орфографии текста в Microsoft Word.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
 // We can un-set the "NoProofing" flag to create a portion of text that
 // bypasses the spell checker while completely disabling it.
 builder.getFont().setNoProofing(true);

 builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

 doc.save(getArtifactsDir() + "Font.NoProofing.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getNumberSpacing() {#getNumberSpacing}
```
public int getNumberSpacing()
```


Получает тип интервала отображаемой цифры.

 **Examples:** 

Показывает, как установить тип интервала цифр.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```

**Returns:**
int — Тип интервала цифры, отображаемой. Возвращаемое значение является одной из констант [NumSpacing](../../com.aspose.words/numspacing/).
### getOldOn() {#getOldOn}
```
public boolean getOldOn()
```




**Returns:**
boolean
### getOldOpacity() {#getOldOpacity}
```
public double getOldOpacity()
```




**Returns:**
double
### getOutline() {#getOutline}
```
public boolean getOutline()
```


True, если шрифт отформатирован как контур.

 **Examples:** 

Показывает, как создать фрагмент текста, отформатированный как контур.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Outline flag to change the text's fill color to white and
 // leave a thin outline around each character in the original color of the text.
 builder.getFont().setOutline(true);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has an outline.");

 doc.save(getArtifactsDir() + "Font.Outline.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPosition() {#getPosition}
```
public double getPosition()
```


Получает позицию текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, отрицательное — опускает.

 **Examples:** 

Показывает, как отформатировать текст, сместив его позицию.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
double — Позиция текста (в пунктах) относительно базовой линии.
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```




**Returns:**
int
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getScaling() {#getScaling}
```
public int getScaling()
```


Получает масштабирование ширины символов в процентах.

 **Examples:** 

Показывает, как задать горизонтальное масштабирование и интервал между символами.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Returns:**
int — Масштаб ширины символа в процентах.
### getShading() {#getShading}
```
public Shading getShading()
```


Возвращает объект [Shading](../../com.aspose.words/shading/), который относится к форматированию затенения для шрифта.

 **Examples:** 

Показывает, как применить затенение к тексту, созданному построителем документов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setColor(Color.WHITE);

 // One way to make the text created using our white font color visible
 // is to apply a background shading effect.
 Shading shading = builder.getFont().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_UP);
 shading.setBackgroundPatternColor(Color.RED);
 shading.setForegroundPatternColor(Color.BLUE);

 builder.writeln("White text on an orange background with a two-tone texture.");

 doc.save(getArtifactsDir() + "Font.Shading.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the font.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


True, если шрифт отформатирован как с тенью.

 **Examples:** 

Показывает, как создать фрагмент текста, отформатированный с тенью.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Shadow flag to apply an offset shadow effect,
 // making it look like the letters are floating above the page.
 builder.getFont().setShadow(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has a shadow.");

 doc.save(getArtifactsDir() + "Font.Shadow.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSize() {#getSize}
```
public double getSize()
```


Получает размер шрифта в пунктах.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
double — Размер шрифта в пунктах.
### getSizeBi() {#getSizeBi}
```
public double getSizeBi()
```


Получает размер шрифта в пунктах, используемый в документе с направлением справа налево.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
double — Размер шрифта в пунктах, используемый в документе с направлением справа налево.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


Истина, если шрифт оформлен малыми заглавными буквами.

 **Examples:** 

Показывает, как отформатировать фрагмент текста для отображения его содержимого заглавными буквами.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Указывает, следует ли текущему шрифту использовать настройки количества символов в строке сетки документа при размещении.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Получает интервал (в пунктах) между символами.

 **Examples:** 

Показывает, как задать горизонтальное масштабирование и интервал между символами.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Returns:**
double — Интервал (в пунктах) между символами.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


Истина, если шрифт оформлен как перечёркнутый.

 **Examples:** 

Показывает, как добавить зачёркнутую линию к тексту.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Получает стиль символов, примененный к этому форматированию.

 **Examples:** 

Применяет двойное подчеркивание ко всем фрагментам в документе, отформатированным пользовательскими стилями символов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a custom style and apply it to text created using a document builder.
 Style style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 builder.getFont().setStyleName("MyStyle");
 builder.write("This text is in a custom style.");

 // Iterate over every run and add a double underline to every custom style.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     Style charStyle = run.getFont().getStyle();

     if (!charStyle.getBuiltIn())
         run.getFont().setUnderline(Underline.DOUBLE);
 }

 doc.save(getArtifactsDir() + "Font.Style.docx");
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The character style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Получает независимый от локали идентификатор стиля символов, примененный к этому форматированию.

 **Examples:** 

Показывает, как изменить стиль существующего текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Returns:**
int — Независимый от локали идентификатор стиля символов, применяемый к этому форматированию. Возвращаемое значение является одной из констант [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Получает имя стиля символов, примененного к этому форматированию.

 **Examples:** 

Показывает, как изменить стиль существующего текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Returns:**
java.lang.String — Имя стиля символов, применяемого к этому форматированию.
### getSubscript() {#getSubscript}
```
public boolean getSubscript()
```


Истина, если шрифт отформатирован как нижний индекс.

 **Examples:** 

Показывает, как отформатировать текст, сместив его позицию.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSuperscript() {#getSuperscript}
```
public boolean getSuperscript()
```


Истина, если шрифт отформатирован как верхний индекс.

 **Examples:** 

Показывает, как отформатировать текст, сместив его позицию.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getTextEffect() {#getTextEffect}
```
public int getTextEffect()
```


Получает эффект анимации шрифта.

 **Examples:** 

Показывает, как применить визуальный эффект к фрагменту.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```

**Returns:**
int — Эффект анимации шрифта. Возвращаемое значение является одной из констант [TextEffect](../../com.aspose.words/texteffect/).
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Получает цвет темы в примененной цветовой схеме, связанной с объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Показывает, как создавать и использовать стили темы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Returns:**
int — Цвет темы в примененной цветовой схеме, связанный с этим объектом [Font](../../com.aspose.words/font/). Возвращаемое значение является одной из констант [ThemeColor](../../com.aspose.words/themecolor/).
### getThemeFont() {#getThemeFont}
```
public int getThemeFont()
```


Получает шрифт темы в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Показывает, как создавать и использовать стили темы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Returns:**
int — Шрифт темы в примененной схеме шрифтов, связанный с этим объектом [Font](../../com.aspose.words/font/). Возвращаемое значение является одной из констант [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontAscii() {#getThemeFontAscii}
```
public int getThemeFontAscii()
```


Получает шрифт темы, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Тема шрифта, используемая для латинского текста (символы с кодами от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Возвращаемое значение является одной из констант [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontBi() {#getThemeFontBi}
```
public int getThemeFontBi()
```


Получает шрифт темы в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/) в документе с языком справа налево.

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Тема шрифта в применяемой схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/) в документе с языком справа налево. Возвращаемое значение является одной из констант [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontFarEast() {#getThemeFontFarEast}
```
public int getThemeFontFarEast()
```


Получает восточноазиатский шрифт темы в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Тема шрифта Восточной Азии в применяемой схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Возвращаемое значение является одной из констант [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontOther() {#getThemeFontOther}
```
public int getThemeFontOther()
```


Получает шрифт темы, используемый для символов с кодами от 128 до 255 в примененной схеме шрифтов, связанной с объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Тема шрифта, используемая для символов с кодами от 128 до 255 в применяемой схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Возвращаемое значение является одной из констант [ThemeFont](../../com.aspose.words/themefont/).
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Получает двойное значение, которое осветляет или затемняет цвет.

**Returns:**
double — двойное значение, которое осветляет или затемняет цвет.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Получает тип подчеркивания, примененного к шрифту.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как вставить поле гиперссылки.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Показывает, как настроить стиль и цвет подчеркивания текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
int - Тип подчеркивания, применяемого к шрифту. Возвращаемое значение является одной из констант [Underline](../../com.aspose.words/underline/).
### getUnderlineColor() {#getUnderlineColor}
```
public Color getUnderlineColor()
```


Получает цвет подчеркивания, примененного к шрифту.

 **Examples:** 

Показывает, как настроить стиль и цвет подчеркивания текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
java.awt.Color - Цвет подчеркивания, применяемого к шрифту.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectType | int |  |

**Returns:**
boolean
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| стиль | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean}
```
public void setAllCaps(boolean value)
```


True, если шрифт отформатирован заглавными буквами.

 **Examples:** 

Показывает, как отформатировать фрагмент текста для отображения его содержимого заглавными буквами.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Указывает, должны ли содержимое этого фрагмента иметь характеристики справа налево.

 **Remarks:** 

Это свойство, когда включено, не должно использоваться с сильно направленным слева направо текстом. Любое поведение в этом случае не определено. Это свойство, когда выключено, не должно использоваться с сильным текстом справа налево. Любое поведение в этом случае не определено.

Когда содержимое этого фрагмента отображается, все символы должны рассматриваться как символы сложного скрипта для целей форматирования. Это означает, что [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) и соответствующее имя шрифта будут использоваться при рендеринге этого фрагмента.

Также, когда содержимое этого фрагмента отображается, это свойство действует как переопределение справа налево для символов, классифицированных как "слабые типы" и "нейтральные типы".

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True, если шрифт оформлен как жирный.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setBoldBi(boolean value) {#setBoldBi-boolean}
```
public void setBoldBi(boolean value)
```


True, если текст справа налево отформатирован полужирным.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |
| значение | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Устанавливает цвет шрифта.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как вставить поле гиперссылки.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет шрифта. |

### setComplexScript(boolean value) {#setComplexScript-boolean}
```
public void setComplexScript(boolean value)
```


Указывает, следует ли рассматривать содержимое этого фрагмента как текст сложного скрипта независимо от их значений Unicode при определении форматирования этого фрагмента.

 **Examples:** 

Показывает, как добавить текст, который всегда рассматривается как сложный скрипт.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean}
```
public void setDoubleStrikeThrough(boolean value)
```


True, если шрифт отформатирован двойным зачеркиванием.

 **Examples:** 

Показывает, как добавить зачёркнутую линию к тексту.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setEmboss(boolean value) {#setEmboss-boolean}
```
public void setEmboss(boolean value)
```


True, если шрифт отформатирован как рельефный.

 **Examples:** 

Показывает, как применить эффекты гравировки/тиснения к тексту.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setEmphasisMark(int value) {#setEmphasisMark-int}
```
public void setEmphasisMark(int value)
```


Устанавливает знак акцента, применяемый к этому форматированию.

 **Examples:** 

Показывает, как добавить дополнительный символ, отображаемый над/под глифом.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Маркер акцента, применяемый к этому форматированию. Значение должно быть одной из констант [EmphasisMark](../../com.aspose.words/emphasismark/). |

### setEngrave(boolean value) {#setEngrave-boolean}
```
public void setEngrave(boolean value)
```


True, если шрифт отформатирован как гравированный.

 **Examples:** 

Показывает, как применить эффекты гравировки/тиснения к тексту.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double |  |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


True, если шрифт отформатирован как скрытый текст.

 **Examples:** 

Показывает, как создать фрагмент скрытого текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
 // We will not see or highlight hidden text unless we enable the "Hidden text" option
 // found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
 // and we will be able to access this text programmatically.
 // It is not advised to use this method to hide sensitive information.
 builder.getFont().setHidden(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text will not be visible in the document.");

 doc.save(getArtifactsDir() + "Font.Hidden.docx");
 
```

Показывает, как использовать реализацию DocumentVisitor для удаления всего скрытого содержимого из документа.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color}
```
public void setHighlightColor(Color value)
```


Устанавливает цвет выделения (маркировки).

 **Examples:** 

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет выделения (маркер). |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Истина, если шрифт оформлен курсивом.

 **Examples:** 

Показывает, как написать курсивный текст с помощью document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setItalicBi(boolean value) {#setItalicBi-boolean}
```
public void setItalicBi(boolean value)
```


True, если текст справа налево отформатирован как курсив.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setKerning(double value) {#setKerning-double}
```
public void setKerning(double value)
```


Устанавливает размер шрифта, при котором начинается кёрнинг.

 **Examples:** 

Показывает, как указать размер шрифта, при котором начинается кернинг.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial Black");

 // Set the builder's font size, and minimum size at which kerning will take effect.
 // The font size falls below the kerning threshold, so the run bellow will not have kerning.
 builder.getFont().setSize(18.0);
 builder.getFont().setKerning(24.0);

 builder.writeln("TALLY. (Kerning not applied)");

 // Set the kerning threshold so that the builder's current font size is above it.
 // Any text we add from this point will have kerning applied. The spaces between characters
 // will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
 builder.getFont().setKerning(12.0);

 builder.writeln("TALLY. (Kerning applied)");

 doc.save(getArtifactsDir() + "Font.Kerning.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Размер шрифта, при котором начинается кернинг. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Устанавливает идентификатор локали (язык) отформатированных символов.

 **Remarks:** 

Список идентификаторов локали см. https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Показывает, как установить локаль текста, который мы добавляем с помощью document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we set the font's locale to English and insert some Russian text,
 // the English locale spell checker will not recognize the text and detect it as a spelling error.
 builder.getFont().setLocaleId(1033);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 // Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
 builder.getFont().setLocaleId(1049);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 doc.save(getArtifactsDir() + "Font.LocaleId.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Идентификатор локали (язык) отформатированных символов. |

### setLocaleIdBi(int value) {#setLocaleIdBi-int}
```
public void setLocaleIdBi(int value)
```


Устанавливает идентификатор локали (язык) отформатированных символов справа налево.

 **Remarks:** 

Список идентификаторов локали см. https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Идентификатор локали (язык) отформатированных символов справа налево. |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int}
```
public void setLocaleIdFarEast(int value)
```


Устанавливает идентификатор локали (язык) отформатированных азиатских символов.

 **Remarks:** 

Список идентификаторов локали см. https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Показывает, как вставлять и форматировать текст на языке Дальнего Востока.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Идентификатор локали (язык) отформатированных азиатских символов. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Устанавливает имя шрифта.

 **Remarks:** 

При получении возвращает [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

При установке задает [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) и [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) указанным значением.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя шрифта. |

### setNameAscii(String value) {#setNameAscii-java.lang.String}
```
public void setNameAscii(String value)
```


Устанавливает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127).

 **Examples:** 

Показывает, как Microsoft Word может объединять два разных шрифта в одном фрагменте.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |

### setNameBi(String value) {#setNameBi-java.lang.String}
```
public void setNameBi(String value)
```


Устанавливает имя шрифта в документе с языком, пишущимся справа налево.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя шрифта в документе с языком справа налево. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String}
```
public void setNameFarEast(String value)
```


Устанавливает имя восточноазиатского шрифта.

 **Examples:** 

Показывает, как вставлять и форматировать текст на языке Дальнего Востока.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя шрифта Восточной Азии. |

### setNameOther(String value) {#setNameOther-java.lang.String}
```
public void setNameOther(String value)
```


Устанавливает шрифт, используемый для символов с кодами от 128 до 255.

 **Examples:** 

Показывает, как Microsoft Word может объединять два разных шрифта в одном фрагменте.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Шрифт, используемый для символов с кодами от 128 до 255. |

### setNoProofing(boolean value) {#setNoProofing-boolean}
```
public void setNoProofing(boolean value)
```


True, когда отформатированные символы не подлежат проверке орфографии.

 **Examples:** 

Показывает, как предотвратить проверку орфографии текста в Microsoft Word.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
 // We can un-set the "NoProofing" flag to create a portion of text that
 // bypasses the spell checker while completely disabling it.
 builder.getFont().setNoProofing(true);

 builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

 doc.save(getArtifactsDir() + "Font.NoProofing.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setNumberSpacing(int value) {#setNumberSpacing-int}
```
public void setNumberSpacing(int value)
```


Устанавливает тип интервала цифры, отображаемой.

 **Examples:** 

Показывает, как установить тип интервала цифр.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Тип интервала цифр, отображаемых в числе. Значение должно быть одной из констант [NumSpacing](../../com.aspose.words/numspacing/). |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double |  |

### setOutline(boolean value) {#setOutline-boolean}
```
public void setOutline(boolean value)
```


True, если шрифт отформатирован как контур.

 **Examples:** 

Показывает, как создать фрагмент текста, отформатированный как контур.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Outline flag to change the text's fill color to white and
 // leave a thin outline around each character in the original color of the text.
 builder.getFont().setOutline(true);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has an outline.");

 doc.save(getArtifactsDir() + "Font.Outline.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setPosition(double value) {#setPosition-double}
```
public void setPosition(double value)
```


Устанавливает позицию текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, отрицательное опускает его.

 **Examples:** 

Показывает, как отформатировать текст, сместив его позицию.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Позиция текста (в пунктах) относительно базовой линии. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean |  |

### setScaling(int value) {#setScaling-int}
```
public void setScaling(int value)
```


Устанавливает масштабирование ширины символов в процентах.

 **Examples:** 

Показывает, как задать горизонтальное масштабирование и интервал между символами.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Масштабирование ширины символов в процентах. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


True, если шрифт отформатирован как с тенью.

 **Examples:** 

Показывает, как создать фрагмент текста, отформатированный с тенью.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Shadow flag to apply an offset shadow effect,
 // making it look like the letters are floating above the page.
 builder.getFont().setShadow(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has a shadow.");

 doc.save(getArtifactsDir() + "Font.Shadow.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Устанавливает размер шрифта в пунктах.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как форматировать последовательность текста, используя её свойство шрифта.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Размер шрифта в пунктах. |

### setSizeBi(double value) {#setSizeBi-double}
```
public void setSizeBi(double value)
```


Устанавливает размер шрифта в пунктах, используемый в документе с языком, пишущимся справа налево.

 **Examples:** 

Показывает, как определить отдельные наборы параметров шрифта для текста справа налево и текста слева направо.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Размер шрифта в пунктах, используемый в документе с написанием справа налево. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


Истина, если шрифт оформлен малыми заглавными буквами.

 **Examples:** 

Показывает, как отформатировать фрагмент текста для отображения его содержимого заглавными буквами.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Указывает, следует ли текущему шрифту использовать настройки количества символов в строке сетки документа при размещении.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Устанавливает интервал (в пунктах) между символами.

 **Examples:** 

Показывает, как задать горизонтальное масштабирование и интервал между символами.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Интервал (в пунктах) между символами. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


Истина, если шрифт оформлен как перечёркнутый.

 **Examples:** 

Показывает, как добавить зачёркнутую линию к тексту.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Устанавливает стиль символов, применяемый к этому форматированию.

 **Examples:** 

Применяет двойное подчеркивание ко всем фрагментам в документе, отформатированным пользовательскими стилями символов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a custom style and apply it to text created using a document builder.
 Style style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 builder.getFont().setStyleName("MyStyle");
 builder.write("This text is in a custom style.");

 // Iterate over every run and add a double underline to every custom style.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     Style charStyle = run.getFont().getStyle();

     if (!charStyle.getBuiltIn())
         run.getFont().setUnderline(Underline.DOUBLE);
 }

 doc.save(getArtifactsDir() + "Font.Style.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | Стиль символов, примененный к этому форматированию. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Устанавливает независимый от локали идентификатор стиля символов, применяемый к этому форматированию.

 **Examples:** 

Показывает, как изменить стиль существующего текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Независимый от локали идентификатор стиля символов, примененный к этому форматированию. Значение должно быть одним из констант [StyleIdentifier](../../com.aspose.words/styleidentifier/). |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Устанавливает имя стиля символов, применяемого к этому форматированию.

 **Examples:** 

Показывает, как изменить стиль существующего текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя стиля символов, примененного к этому форматированию. |

### setSubscript(boolean value) {#setSubscript-boolean}
```
public void setSubscript(boolean value)
```


Истина, если шрифт отформатирован как нижний индекс.

 **Examples:** 

Показывает, как отформатировать текст, сместив его позицию.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSuperscript(boolean value) {#setSuperscript-boolean}
```
public void setSuperscript(boolean value)
```


Истина, если шрифт отформатирован как верхний индекс.

 **Examples:** 

Показывает, как отформатировать текст, сместив его позицию.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setTextEffect(int value) {#setTextEffect-int}
```
public void setTextEffect(int value)
```


Устанавливает эффект анимации шрифта.

 **Examples:** 

Показывает, как применить визуальный эффект к фрагменту.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Эффект анимации шрифта. Значение должно быть одним из констант [TextEffect](../../com.aspose.words/texteffect/). |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Устанавливает цвет темы в примененной цветовой схеме, связанной с этим объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Показывает, как создавать и использовать стили темы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Цвет темы в примененной цветовой схеме, связанной с этим объектом [Font](../../com.aspose.words/font/). Значение должно быть одним из констант [ThemeColor](../../com.aspose.words/themecolor/). |

### setThemeFont(int value) {#setThemeFont-int}
```
public void setThemeFont(int value)
```


Устанавливает шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Показывает, как создавать и использовать стили темы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Значение должно быть одним из констант [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontAscii(int value) {#setThemeFontAscii-int}
```
public void setThemeFontAscii(int value)
```


Устанавливает шрифт темы, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Шрифт темы, используемый для латинского текста (символы с кодами от 0 (ноль) до 127) в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Значение должно быть одним из констант [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontBi(int value) {#setThemeFontBi-int}
```
public void setThemeFontBi(int value)
```


Устанавливает шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/) в документе с языком, пишущимся справа налево.

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/) в документе на языке с написанием справа налево. Значение должно быть одним из констант [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int}
```
public void setThemeFontFarEast(int value)
```


Устанавливает восточноазиатский шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Восточноазиатский шрифт темы в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Значение должно быть одним из констант [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontOther(int value) {#setThemeFontOther-int}
```
public void setThemeFontOther(int value)
```


Устанавливает шрифт темы, используемый для символов с кодами от 128 до 255 в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/).

 **Examples:** 

Показывает, как работать с шрифтами темы и цветами.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Шрифт темы, используемый для символов с кодами от 128 до 255 в примененной схеме шрифтов, связанной с этим объектом [Font](../../com.aspose.words/font/). Значение должно быть одним из констант [ThemeFont](../../com.aspose.words/themefont/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Устанавливает двойное значение, которое осветляет или затемняет цвет.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Двойное значение, которое осветляет или затемняет цвет. |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Устанавливает тип подчеркивания, применяемый к шрифту.

 **Examples:** 

Показывает, как вставлять отформатированный текст с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Показывает, как вставить поле гиперссылки.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Показывает, как настроить стиль и цвет подчеркивания текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Тип подчеркивания, применяемого к шрифту. Значение должно быть одним из констант [Underline](../../com.aspose.words/underline/). |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color}
```
public void setUnderlineColor(Color value)
```


Устанавливает цвет подчеркивания, применяемого к шрифту.

 **Examples:** 

Показывает, как настроить стиль и цвет подчеркивания текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет подчеркивания, применяемого к шрифту. |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| стиль | int |  |
| variant | int |  |

