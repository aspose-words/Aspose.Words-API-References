---
title: Font
second_title: Справочник по API Aspose.Words для Java
description: Содержит атрибуты шрифта, имя шрифта, размер шрифта, цвет и т. д. для объекта.
type: docs
weight: 275
url: /ru/java/com.aspose.words/font/
---

**Наследование:**
java.lang.Object
```
public class Font
```

Содержит атрибуты шрифта (имя шрифта, размер шрифта, цвет и т. д.) для объекта.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

 Вы не создаете экземпляры[Font](../../com.aspose.words/font) класс напрямую. Вы просто используете[Font](../../com.aspose.words/font) для доступа к свойствам шрифта различных объектов, таких как[Run](../../com.aspose.words/run), [Paragraph](../../com.aspose.words/paragraph), [Style](../../com.aspose.words/style), [DocumentBuilder](../../com.aspose.words/documentbuilder).
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Сбрасывает форматирование шрифта по умолчанию. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [getAllCaps()](#getAllCaps--) | Истинно, если шрифт отформатирован как все заглавные буквы. |
| [getAutoColor()](#getAutoColor--) | Возвращает текущий рассчитанный цвет текста (черный или белый), который будет использоваться для «автоцвета». |
| [getBidi()](#getBidi--) | Указывает, должно ли содержимое этого цикла иметь характеристики письма справа налево. |
| [getBold()](#getBold--) | Истинно, если шрифт отформатирован как полужирный. |
| [getBoldBi()](#getBoldBi--) | Истинно, если текст справа налево выделен полужирным шрифтом. |
| [getBorder()](#getBorder--) | Возвращает объект Border, указывающий границу для шрифта. |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает цвет шрифта. |
| [getComplexScript()](#getComplexScript--) | Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст скрипта независимо от их значений символов Unicode при определении форматирования для этого запуска. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough--) | Истинно, если шрифт отформатирован как двойной зачеркнутый текст. |
| [getEmboss()](#getEmboss--) | Истинно, если шрифт отформатирован как рельефный. |
| [getEmphasisMark()](#getEmphasisMark--) | Получает знак акцента, применяемый к этому форматированию. |
| [getEngrave()](#getEngrave--) | Истинно, если шрифт отформатирован как выгравированный. |
| [getFill()](#getFill--) | Получает форматирование заливки для шрифта. |
| [getFillType()](#getFillType--) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [getFilledColor()](#getFilledColor--) |  |
| [getGradientAngle()](#getGradientAngle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getHidden()](#getHidden--) | Истинно, если шрифт отформатирован как скрытый текст. |
| [getHighlightColor()](#getHighlightColor--) | Получает цвет выделения (маркера). |
| [getItalic()](#getItalic--) | Истинно, если шрифт отформатирован как курсив. |
| [getItalicBi()](#getItalicBi--) | Истина, если текст справа налево отформатирован курсивом. |
| [getKerning()](#getKerning--) | Получает размер шрифта, с которого начинается кернинг. |
| [getLineSpacing()](#getLineSpacing--) | Возвращает межстрочный интервал данного шрифта (в пунктах). |
| [getLocaleId()](#getLocaleId--) | Получает идентификатор локали (язык) отформатированных символов. |
| [getLocaleIdBi()](#getLocaleIdBi--) | Получает идентификатор локали (язык) отформатированных символов, написанных справа налево. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast--) | Получает идентификатор локали (язык) отформатированных азиатских символов. |
| [getName()](#getName--) | Получает имя шрифта. |
| [getNameAscii()](#getNameAscii--) | Получает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |
| [getNameBi()](#getNameBi--) | Получает имя шрифта в документе на языке с написанием справа налево. |
| [getNameFarEast()](#getNameFarEast--) | Получает имя восточноазиатского шрифта. |
| [getNameOther()](#getNameOther--) | Получает шрифт, используемый для символов с кодами символов от 128 до 255. |
| [getNoProofing()](#getNoProofing--) | Истинно, если отформатированные символы не должны проверяться на орфографию. |
| [getOn()](#getOn--) |  |
| [getOpacity()](#getOpacity--) |  |
| [getOutline()](#getOutline--) | Истинно, если шрифт отформатирован как контур. |
| [getPatternType()](#getPatternType--) |  |
| [getPosition()](#getPosition--) | Получает положение текста (в пунктах) относительно базовой линии. |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [getScaling()](#getScaling--) | Получает масштабирование ширины символа в процентах. |
| [getShading()](#getShading--) | Возвращает объект Shading, который ссылается на форматирование заливки для шрифта. |
| [getShadow()](#getShadow--) | Истинно, если шрифт отформатирован как затененный. |
| [getSize()](#getSize--) | Получает размер шрифта в пунктах. |
| [getSizeBi()](#getSizeBi--) | Получает размер шрифта в пунктах, используемый в документе с письмом справа налево. |
| [getSmallCaps()](#getSmallCaps--) | Истинно, если шрифт отформатирован как маленькие заглавные буквы. |
| [getSnapToGrid()](#getSnapToGrid--) | Указывает, должен ли текущий шрифт использовать параметры сетки документа на строку при компоновке. |
| [getSpacing()](#getSpacing--) | Получает расстояние (в пунктах) между символами. |
| [getStrikeThrough()](#getStrikeThrough--) | Истинно, если шрифт отформатирован как зачеркнутый текст. |
| [getStyle()](#getStyle--) | Получает стиль символа, применяемый к этому форматированию. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Получает независимый от языкового стандарта идентификатор стиля символа, примененного к этому форматированию. |
| [getStyleName()](#getStyleName--) | Получает имя стиля символа, примененного к этому форматированию. |
| [getSubscript()](#getSubscript--) | Истинно, если шрифт отформатирован как нижний индекс. |
| [getSuperscript()](#getSuperscript--) | Истинно, если шрифт отформатирован как надстрочный. |
| [getTextEffect()](#getTextEffect--) | Получает эффект анимации шрифта. |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [getThemeColor()](#getThemeColor--) | Получает цвет темы в применяемой цветовой схеме, связанной с этим объектом Font. |
| [getThemeFont()](#getThemeFont--) | Получает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [getThemeFontAscii()](#getThemeFontAscii--) | Получает шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [getThemeFontBi()](#getThemeFontBi--) | Получает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font в документе на языке с письмом справа налево. |
| [getThemeFontFarEast()](#getThemeFontFarEast--) | Получает шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [getThemeFontOther()](#getThemeFontOther--) | Получает шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифта, связанной с этим объектом Font. |
| [getTintAndShade()](#getTintAndShade--) | Получает двойное значение, которое делает цвет светлее или темнее. |
| [getUnderline()](#getUnderline--) | Получает тип подчеркивания, примененного к шрифту. |
| [getUnderlineColor()](#getUnderlineColor--) | Получает цвет подчеркивания, примененного к шрифту. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int-) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [patterned(int patternType)](#patterned-int-) |  |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean-) | Истинно, если шрифт отформатирован как все заглавные буквы. |
| [setBidi(boolean value)](#setBidi-boolean-) | Указывает, должно ли содержимое этого цикла иметь характеристики письма справа налево. |
| [setBold(boolean value)](#setBold-boolean-) | Истинно, если шрифт отформатирован как полужирный. |
| [setBoldBi(boolean value)](#setBoldBi-boolean-) | Истинно, если текст справа налево выделен полужирным шрифтом. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | Устанавливает цвет шрифта. |
| [setComplexScript(boolean value)](#setComplexScript-boolean-) | Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст скрипта независимо от их значений символов Unicode при определении форматирования для этого запуска. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean-) | Истинно, если шрифт отформатирован как двойной зачеркнутый текст. |
| [setEmboss(boolean value)](#setEmboss-boolean-) | Истинно, если шрифт отформатирован как рельефный. |
| [setEmphasisMark(int value)](#setEmphasisMark-int-) | Устанавливает знак акцента, применяемый к этому форматированию. |
| [setEngrave(boolean value)](#setEngrave-boolean-) | Истинно, если шрифт отформатирован как выгравированный. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [setHidden(boolean value)](#setHidden-boolean-) | Истинно, если шрифт отформатирован как скрытый текст. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color-) | Устанавливает цвет выделения (маркера). |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [setItalic(boolean value)](#setItalic-boolean-) | Истинно, если шрифт отформатирован как курсив. |
| [setItalicBi(boolean value)](#setItalicBi-boolean-) | Истина, если текст справа налево отформатирован курсивом. |
| [setKerning(double value)](#setKerning-double-) | Устанавливает размер шрифта, с которого начинается кернинг. |
| [setLocaleId(int value)](#setLocaleId-int-) | Задает идентификатор локали (язык) отформатированных символов. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int-) | Задает идентификатор локали (язык) отформатированных символов, написанных справа налево. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int-) | Задает идентификатор локали (язык) отформатированных азиатских символов. |
| [setName(String value)](#setName-java.lang.String-) | Устанавливает имя шрифта. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String-) | Устанавливает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |
| [setNameBi(String value)](#setNameBi-java.lang.String-) | Задает имя шрифта в документе на языке с письмом справа налево. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String-) | Задает имя восточноазиатского шрифта. |
| [setNameOther(String value)](#setNameOther-java.lang.String-) | Устанавливает шрифт, используемый для символов с кодами символов от 128 до 255. |
| [setNoProofing(boolean value)](#setNoProofing-boolean-) | Истинно, если отформатированные символы не должны проверяться на орфографию. |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [setOutline(boolean value)](#setOutline-boolean-) | Истинно, если шрифт отформатирован как контур. |
| [setPosition(double value)](#setPosition-double-) | Устанавливает положение текста (в пунктах) относительно базовой линии. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [setScaling(int value)](#setScaling-int-) | Устанавливает масштабирование ширины символов в процентах. |
| [setShadow(boolean value)](#setShadow-boolean-) | Истинно, если шрифт отформатирован как затененный. |
| [setSize(double value)](#setSize-double-) | Устанавливает размер шрифта в пунктах. |
| [setSizeBi(double value)](#setSizeBi-double-) | Устанавливает размер шрифта в пунктах, используемых в документе с написанием справа налево. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean-) | Истинно, если шрифт отформатирован как маленькие заглавные буквы. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean-) | Указывает, должен ли текущий шрифт использовать параметры сетки документа на строку при компоновке. |
| [setSpacing(double value)](#setSpacing-double-) | Устанавливает интервал (в пунктах) между символами. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean-) | Истинно, если шрифт отформатирован как зачеркнутый текст. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Задает стиль символов, применяемый к этому форматированию. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | Задает независимый от локали идентификатор стиля символа, примененного к этому форматированию. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Задает имя стиля символов, применяемого к этому форматированию. |
| [setSubscript(boolean value)](#setSubscript-boolean-) | Истинно, если шрифт отформатирован как нижний индекс. |
| [setSuperscript(boolean value)](#setSuperscript-boolean-) | Истинно, если шрифт отформатирован как надстрочный. |
| [setTextEffect(int value)](#setTextEffect-int-) | Устанавливает эффект анимации шрифта. |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [setThemeColor(int value)](#setThemeColor-int-) | Задает цвет темы в применяемой цветовой схеме, связанной с этим объектом Font. |
| [setThemeFont(int value)](#setThemeFont-int-) | Задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int-) | Задает шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [setThemeFontBi(int value)](#setThemeFontBi-int-) | Задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font в документе на языке с письмом справа налево. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int-) | Задает шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [setThemeFontOther(int value)](#setThemeFontOther-int-) | Задает шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [setTintAndShade(double value)](#setTintAndShade-double-) | Устанавливает двойное значение, которое делает цвет светлее или темнее. |
| [setUnderline(int value)](#setUnderline-int-) | Устанавливает тип подчеркивания, применяемого к шрифту. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color-) | Устанавливает цвет подчеркивания, применяемого к шрифту. |
| [solid()](#solid--) |  |
| [toString()](#toString--) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Сбрасывает форматирование шрифта по умолчанию.

Удаляет все форматирование шрифта, указанное явно для объекта, из которого**Font** был получен, поэтому форматирование шрифта будет унаследовано от соответствующего родителя.

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
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getAllCaps() {#getAllCaps--}
```
public boolean getAllCaps()
```


Истинно, если шрифт отформатирован как все заглавные буквы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getAutoColor() {#getAutoColor--}
```
public Color getAutoColor()
```


 Возвращает текущий рассчитанный цвет текста (черный или белый), который будет использоваться для «автоцвета». Если цвет не «авто», возвращается[getColor()](../../com.aspose.words/font\#getColor--) / [setColor(java.awt.Color)](../../com.aspose.words/font\#setColor-java.awt.Color-).

Когда текст имеет «автоматический цвет», фактический цвет текста рассчитывается автоматически, чтобы его можно было прочитать на фоне цвета фона. Когда вы меняете цвет фона, цвет текста автоматически меняется на черный или белый в MS Word, чтобы обеспечить максимальную читаемость.

**Возвращает:**
java.awt.Color — Текущий вычисленный цвет текста (черный или белый), который будет использоваться для «автоматического цвета».
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Указывает, должно ли содержимое этого цикла иметь характеристики письма справа налево.

Если это свойство включено, его нельзя использовать с текстом, написанным строго слева направо. Любое поведение в этом состоянии не определено. Если это свойство отключено, его нельзя использовать с сильным текстом, написанным справа налево. Любое поведение в этом состоянии не определено.

При отображении содержимого этого цикла все символы должны рассматриваться как сложные символы сценария для целей форматирования. Это означает, что[getBoldBi()](../../com.aspose.words/font\#getBoldBi--) / [setBoldBi(boolean)](../../com.aspose.words/font\#setBoldBi-boolean-), [getItalicBi()](../../com.aspose.words/font\#getItalicBi--) / [setItalicBi(boolean)](../../com.aspose.words/font\#setItalicBi-boolean-), [getSizeBi()](../../com.aspose.words/font\#getSizeBi--) / [setSizeBi(double)](../../com.aspose.words/font\#setSizeBi-double-) и соответствующее имя шрифта будет использоваться при рендеринге этого прогона.

Кроме того, когда отображается содержимое этого цикла, это свойство действует как переопределение справа налево для символов, которые классифицируются как «слабые типы» и «нейтральные типы».

**Возвращает:**
boolean - соответствующее логическое значение.
### getBold() {#getBold--}
```
public boolean getBold()
```


Истинно, если шрифт отформатирован как полужирный.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBoldBi() {#getBoldBi--}
```
public boolean getBoldBi()
```


Истинно, если текст справа налево выделен полужирным шрифтом.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorder() {#getBorder--}
```
public Border getBorder()
```


Возвращает объект Border, указывающий границу для шрифта.

**Возвращает:**
[Border](../../com.aspose.words/border) - Объект Border, указывающий границу для шрифта.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColor() {#getColor--}
```
public Color getColor()
```


Получает цвет шрифта.

**Возвращает:**
java.awt.Color — цвет шрифта.
### getComplexScript() {#getComplexScript--}
```
public boolean getComplexScript()
```


Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст скрипта независимо от их значений символов Unicode при определении форматирования для этого запуска.

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
### getDoubleStrikeThrough() {#getDoubleStrikeThrough--}
```
public boolean getDoubleStrikeThrough()
```


Истинно, если шрифт отформатирован как двойной зачеркнутый текст.

**Возвращает:**
boolean - соответствующее логическое значение.
### getEmboss() {#getEmboss--}
```
public boolean getEmboss()
```


Истинно, если шрифт отформатирован как рельефный.

**Возвращает:**
boolean - соответствующее логическое значение.
### getEmphasisMark() {#getEmphasisMark--}
```
public int getEmphasisMark()
```


Получает знак акцента, применяемый к этому форматированию.

**Возвращает:**
 int - Знак акцента, примененный к этому форматированию. Возвращаемое значение является одним из[EmphasisMark](../../com.aspose.words/emphasismark) константы.
### getEngrave() {#getEngrave--}
```
public boolean getEngrave()
```


Истинно, если шрифт отформатирован как выгравированный.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFill() {#getFill--}
```
public Fill getFill()
```


Получает форматирование заливки для шрифта.

**Возвращает:**
[Fill](../../com.aspose.words/fill) - Заполнить форматирование шрифта.
### getFillType() {#getFillType--}
```
public int getFillType()
```




**Возвращает:**
инт
### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**Возвращает:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**Возвращает:**
java.awt.Color
### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**Возвращает:**
байт[]
### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**Возвращает:**
двойной
### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**Возвращает:**
логический
### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**Возвращает:**
java.awt.Color
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**Возвращает:**
двойной
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**Возвращает:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**Возвращает:**
инт
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**Возвращает:**
инт
### getHidden() {#getHidden--}
```
public boolean getHidden()
```


Истинно, если шрифт отформатирован как скрытый текст.

**Возвращает:**
boolean - соответствующее логическое значение.
### getHighlightColor() {#getHighlightColor--}
```
public Color getHighlightColor()
```


Получает цвет выделения (маркера).

**Возвращает:**
java.awt.Color — цвет выделения (маркера).
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


Истинно, если шрифт отформатирован как курсив.

**Возвращает:**
boolean - соответствующее логическое значение.
### getItalicBi() {#getItalicBi--}
```
public boolean getItalicBi()
```


Истина, если текст справа налево отформатирован курсивом.

**Возвращает:**
boolean - соответствующее логическое значение.
### getKerning() {#getKerning--}
```
public double getKerning()
```


Получает размер шрифта, с которого начинается кернинг.

**Возвращает:**
double - Размер шрифта, с которого начинается кернинг.
### getLineSpacing() {#getLineSpacing--}
```
public double getLineSpacing()
```


Возвращает межстрочный интервал данного шрифта (в пунктах).

**Возвращает:**
double - межстрочный интервал данного шрифта (в пунктах).
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает идентификатор локали (язык) отформатированных символов. Список идентификаторов локалей см. на странице https://msdn.microsoft.com/en-us/library/cc233965.aspx.

**Возвращает:**
int - Идентификатор локали (языка) отформатированных символов.
### getLocaleIdBi() {#getLocaleIdBi--}
```
public int getLocaleIdBi()
```


Получает идентификатор локали (язык) отформатированных символов, написанных справа налево. Список идентификаторов локалей см. на странице https://msdn.microsoft.com/en-us/library/cc233965.aspx.

**Возвращает:**
int - Идентификатор локали (язык) отформатированных символов справа налево.
### getLocaleIdFarEast() {#getLocaleIdFarEast--}
```
public int getLocaleIdFarEast()
```


Получает идентификатор локали (язык) отформатированных азиатских символов. Список идентификаторов локалей см. на странице https://msdn.microsoft.com/en-us/library/cc233965.aspx.

**Возвращает:**
int - Идентификатор локали (язык) отформатированных азиатских символов.
### getName() {#getName--}
```
public String getName()
```


Получает имя шрифта.

 При получении возвращает[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-).

 При настройке устанавливает[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-), [getNameBi()](../../com.aspose.words/font\#getNameBi--) / [setNameBi(java.lang.String)](../../com.aspose.words/font\#setNameBi-java.lang.String-), [getNameFarEast()](../../com.aspose.words/font\#getNameFarEast--) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font\#setNameFarEast-java.lang.String-) а также[getNameOther()](../../com.aspose.words/font\#getNameOther--) / [setNameOther(java.lang.String)](../../com.aspose.words/font\#setNameOther-java.lang.String-) к указанному значению.

**Возвращает:**
java.lang.String — Имя шрифта.
### getNameAscii() {#getNameAscii--}
```
public String getNameAscii()
```


Получает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127).

**Возвращает:**
java.lang.String — шрифт, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127).
### getNameBi() {#getNameBi--}
```
public String getNameBi()
```


Получает имя шрифта в документе на языке с написанием справа налево.

**Возвращает:**
java.lang.String — имя шрифта в документе на языке с написанием справа налево.
### getNameFarEast() {#getNameFarEast--}
```
public String getNameFarEast()
```


Получает имя восточноазиатского шрифта.

**Возвращает:**
java.lang.String — название восточноазиатского шрифта.
### getNameOther() {#getNameOther--}
```
public String getNameOther()
```


Получает шрифт, используемый для символов с кодами символов от 128 до 255.

**Возвращает:**
java.lang.String — шрифт, используемый для символов с кодами символов от 128 до 255.
### getNoProofing() {#getNoProofing--}
```
public boolean getNoProofing()
```


Истинно, если отформатированные символы не должны проверяться на орфографию.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOn() {#getOn--}
```
public boolean getOn()
```




**Возвращает:**
логический
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**Возвращает:**
двойной
### getOutline() {#getOutline--}
```
public boolean getOutline()
```


Истинно, если шрифт отформатирован как контур.

**Возвращает:**
boolean - соответствующее логическое значение.
### getPatternType() {#getPatternType--}
```
public int getPatternType()
```




**Возвращает:**
инт
### getPosition() {#getPosition--}
```
public double getPosition()
```


Получает положение текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, отрицательное — опускает.

**Возвращает:**
double - Положение текста (в пунктах) относительно базовой линии.
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**Возвращает:**
инт
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**Возвращает:**
логический
### getScaling() {#getScaling--}
```
public int getScaling()
```


Получает масштабирование ширины символа в процентах.

**Возвращает:**
int - Масштабирование ширины символа в процентах.
### getShading() {#getShading--}
```
public Shading getShading()
```


Возвращает объект Shading, который ссылается на форматирование заливки для шрифта.

**Возвращает:**
[Shading](../../com.aspose.words/shading) - Объект Shading, который ссылается на форматирование заливки для шрифта.
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


Истинно, если шрифт отформатирован как затененный.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSize() {#getSize--}
```
public double getSize()
```


Получает размер шрифта в пунктах.

**Возвращает:**
double - Размер шрифта в пунктах.
### getSizeBi() {#getSizeBi--}
```
public double getSizeBi()
```


Получает размер шрифта в пунктах, используемый в документе с письмом справа налево.

**Возвращает:**
double — размер шрифта в пунктах, используемый в документе с написанием справа налево.
### getSmallCaps() {#getSmallCaps--}
```
public boolean getSmallCaps()
```


Истинно, если шрифт отформатирован как маленькие заглавные буквы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSnapToGrid() {#getSnapToGrid--}
```
public boolean getSnapToGrid()
```


Указывает, должен ли текущий шрифт использовать параметры сетки документа на строку при компоновке.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


Получает расстояние (в пунктах) между символами.

**Возвращает:**
double - Расстояние (в пунктах) между символами.
### getStrikeThrough() {#getStrikeThrough--}
```
public boolean getStrikeThrough()
```


Истинно, если шрифт отформатирован как зачеркнутый текст.

**Возвращает:**
boolean - соответствующее логическое значение.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


Получает стиль символа, применяемый к этому форматированию.

**Возвращает:**
[Style](../../com.aspose.words/style) - Стиль символов, примененный к этому форматированию.
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Получает независимый от языкового стандарта идентификатор стиля символа, примененного к этому форматированию.

**Возвращает:**
 int — независимый от локали идентификатор стиля символа, примененного к этому форматированию. Возвращаемое значение является одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы.
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Получает имя стиля символа, примененного к этому форматированию.

**Возвращает:**
java.lang.String — имя стиля символа, примененного к этому форматированию.
### getSubscript() {#getSubscript--}
```
public boolean getSubscript()
```


Истинно, если шрифт отформатирован как нижний индекс.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuperscript() {#getSuperscript--}
```
public boolean getSuperscript()
```


Истинно, если шрифт отформатирован как надстрочный.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTextEffect() {#getTextEffect--}
```
public int getTextEffect()
```


Получает эффект анимации шрифта.

**Возвращает:**
 int - Эффект анимации шрифта. Возвращаемое значение является одним из[TextEffect](../../com.aspose.words/texteffect) константы.
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**Возвращает:**
инт
### getThemeColor() {#getThemeColor--}
```
public int getThemeColor()
```


Получает цвет темы в применяемой цветовой схеме, связанной с этим объектом Font.

**Возвращает:**
int — цвет темы в применяемой цветовой схеме, связанной с этим объектом Font. Возвращаемое значение является одним из[ThemeColor](../../com.aspose.words/themecolor) константы.
### getThemeFont() {#getThemeFont--}
```
public int getThemeFont()
```


Получает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font.

**Возвращает:**
 int — шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font. Возвращаемое значение является одним из[ThemeFont](../../com.aspose.words/themefont) константы.
### getThemeFontAscii() {#getThemeFontAscii--}
```
public int getThemeFontAscii()
```


Получает шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом Font.

**Возвращает:**
 int — шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом Font. Возвращаемое значение является одним из[ThemeFont](../../com.aspose.words/themefont) константы.
### getThemeFontBi() {#getThemeFontBi--}
```
public int getThemeFontBi()
```


Получает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font в документе на языке с письмом справа налево.

**Возвращает:**
 int — шрифт темы в применяемой схеме шрифтов, связанный с этим объектом Font в документе на языке с письмом справа налево. Возвращаемое значение является одним из[ThemeFont](../../com.aspose.words/themefont) константы.
### getThemeFontFarEast() {#getThemeFontFarEast--}
```
public int getThemeFontFarEast()
```


Получает шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font.

**Возвращает:**
 int — шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font. Возвращаемое значение является одним из[ThemeFont](../../com.aspose.words/themefont) константы.
### getThemeFontOther() {#getThemeFontOther--}
```
public int getThemeFontOther()
```


Получает шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифта, связанной с этим объектом Font.

**Возвращает:**
 int — шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифтов, связанной с этим объектом Font. Возвращаемое значение является одним из[ThemeFont](../../com.aspose.words/themefont) константы.
### getTintAndShade() {#getTintAndShade--}
```
public double getTintAndShade()
```


Получает двойное значение, которое делает цвет светлее или темнее.

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) нейтрален. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит к исключению java.lang.IllegalArgumentException.

Установка этого свойства для объекта Font с цветами, не относящимися к теме, приводит к исключению java.lang.IllegalStateException.

**Возвращает:**
double — двойное значение, которое осветляет или затемняет цвет.
### getUnderline() {#getUnderline--}
```
public int getUnderline()
```


Получает тип подчеркивания, примененного к шрифту.

**Возвращает:**
 int — Тип подчеркивания, примененный к шрифту. Возвращаемое значение является одним из[Underline](../../com.aspose.words/underline) константы.
### getUnderlineColor() {#getUnderlineColor--}
```
public Color getUnderlineColor()
```


Получает цвет подчеркивания, примененного к шрифту.

**Возвращает:**
java.awt.Color — цвет подчеркивания шрифта.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int-}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectType | int |  |

**Возвращает:**
логический
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




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double-}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int-}
```
public void patterned(int patternType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean-}
```
public void setAllCaps(boolean value)
```


Истинно, если шрифт отформатирован как все заглавные буквы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Указывает, должно ли содержимое этого цикла иметь характеристики письма справа налево.

Если это свойство включено, его нельзя использовать с текстом, написанным строго слева направо. Любое поведение в этом состоянии не определено. Если это свойство отключено, его нельзя использовать с сильным текстом, написанным справа налево. Любое поведение в этом состоянии не определено.

При отображении содержимого этого цикла все символы должны рассматриваться как сложные символы сценария для целей форматирования. Это означает, что[getBoldBi()](../../com.aspose.words/font\#getBoldBi--) / [setBoldBi(boolean)](../../com.aspose.words/font\#setBoldBi-boolean-), [getItalicBi()](../../com.aspose.words/font\#getItalicBi--) / [setItalicBi(boolean)](../../com.aspose.words/font\#setItalicBi-boolean-), [getSizeBi()](../../com.aspose.words/font\#getSizeBi--) / [setSizeBi(double)](../../com.aspose.words/font\#setSizeBi-double-) и соответствующее имя шрифта будет использоваться при рендеринге этого прогона.

Кроме того, когда отображается содержимое этого цикла, это свойство действует как переопределение справа налево для символов, которые классифицируются как «слабые типы» и «нейтральные типы».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBold(boolean value) {#setBold-boolean-}
```
public void setBold(boolean value)
```


Истинно, если шрифт отформатирован как полужирный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBoldBi(boolean value) {#setBoldBi-boolean-}
```
public void setBoldBi(boolean value)
```


Истинно, если текст справа налево выделен полужирным шрифтом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Устанавливает цвет шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет шрифта. |

### setComplexScript(boolean value) {#setComplexScript-boolean-}
```
public void setComplexScript(boolean value)
```


Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст скрипта независимо от их значений символов Unicode при определении форматирования для этого запуска.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean-}
```
public void setDoubleStrikeThrough(boolean value)
```


Истинно, если шрифт отформатирован как двойной зачеркнутый текст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setEmboss(boolean value) {#setEmboss-boolean-}
```
public void setEmboss(boolean value)
```


Истинно, если шрифт отформатирован как рельефный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setEmphasisMark(int value) {#setEmphasisMark-int-}
```
public void setEmphasisMark(int value)
```


Устанавливает знак акцента, применяемый к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Знак акцента применяется к этому форматированию. Значение должно быть одним из[EmphasisMark](../../com.aspose.words/emphasismark) константы. |

### setEngrave(boolean value) {#setEngrave-boolean-}
```
public void setEngrave(boolean value)
```


Истинно, если шрифт отформатирован как выгравированный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### setHidden(boolean value) {#setHidden-boolean-}
```
public void setHidden(boolean value)
```


Истинно, если шрифт отформатирован как скрытый текст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color-}
```
public void setHighlightColor(Color value)
```


Устанавливает цвет выделения (маркера).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет выделения (маркера). |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


Истинно, если шрифт отформатирован как курсив.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setItalicBi(boolean value) {#setItalicBi-boolean-}
```
public void setItalicBi(boolean value)
```


Истина, если текст справа налево отформатирован курсивом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setKerning(double value) {#setKerning-double-}
```
public void setKerning(double value)
```


Устанавливает размер шрифта, с которого начинается кернинг.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Размер шрифта, с которого начинается кернинг. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Задает идентификатор локали (язык) отформатированных символов. Список идентификаторов локалей см. на странице https://msdn.microsoft.com/en-us/library/cc233965.aspx.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Идентификатор локали (язык) отформатированных символов. |

### setLocaleIdBi(int value) {#setLocaleIdBi-int-}
```
public void setLocaleIdBi(int value)
```


Задает идентификатор локали (язык) отформатированных символов, написанных справа налево. Список идентификаторов локалей см. на странице https://msdn.microsoft.com/en-us/library/cc233965.aspx.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Идентификатор локали (язык) отформатированных символов, написанных справа налево. |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int-}
```
public void setLocaleIdFarEast(int value)
```


Задает идентификатор локали (язык) отформатированных азиатских символов. Список идентификаторов локалей см. на странице https://msdn.microsoft.com/en-us/library/cc233965.aspx.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Идентификатор локали (язык) отформатированных азиатских символов. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Устанавливает имя шрифта.

 При получении возвращает[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-).

 При настройке устанавливает[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-), [getNameBi()](../../com.aspose.words/font\#getNameBi--) / [setNameBi(java.lang.String)](../../com.aspose.words/font\#setNameBi-java.lang.String-), [getNameFarEast()](../../com.aspose.words/font\#getNameFarEast--) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font\#setNameFarEast-java.lang.String-) а также[getNameOther()](../../com.aspose.words/font\#getNameOther--) / [setNameOther(java.lang.String)](../../com.aspose.words/font\#setNameOther-java.lang.String-) к указанному значению.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название шрифта. |

### setNameAscii(String value) {#setNameAscii-java.lang.String-}
```
public void setNameAscii(String value)
```


Устанавливает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |

### setNameBi(String value) {#setNameBi-java.lang.String-}
```
public void setNameBi(String value)
```


Задает имя шрифта в документе на языке с письмом справа налево.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя шрифта в документе на языке с написанием справа налево. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String-}
```
public void setNameFarEast(String value)
```


Задает имя восточноазиатского шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название восточноазиатского шрифта. |

### setNameOther(String value) {#setNameOther-java.lang.String-}
```
public void setNameOther(String value)
```


Устанавливает шрифт, используемый для символов с кодами символов от 128 до 255.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Шрифт, используемый для символов с кодами символов от 128 до 255. |

### setNoProofing(boolean value) {#setNoProofing-boolean-}
```
public void setNoProofing(boolean value)
```


Истинно, если отформатированные символы не должны проверяться на орфографию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### setOutline(boolean value) {#setOutline-boolean-}
```
public void setOutline(boolean value)
```


Истинно, если шрифт отформатирован как контур.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPosition(double value) {#setPosition-double-}
```
public void setPosition(double value)
```


Устанавливает положение текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, отрицательное — опускает.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Положение текста (в пунктах) относительно базовой линии. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setScaling(int value) {#setScaling-int-}
```
public void setScaling(int value)
```


Устанавливает масштабирование ширины символов в процентах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Масштабирование ширины символов в процентах. |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


Истинно, если шрифт отформатирован как затененный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSize(double value) {#setSize-double-}
```
public void setSize(double value)
```


Устанавливает размер шрифта в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Размер шрифта в пунктах. |

### setSizeBi(double value) {#setSizeBi-double-}
```
public void setSizeBi(double value)
```


Устанавливает размер шрифта в пунктах, используемых в документе с написанием справа налево.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Размер шрифта в пунктах, используемый в документе с написанием справа налево. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean-}
```
public void setSmallCaps(boolean value)
```


Истинно, если шрифт отформатирован как маленькие заглавные буквы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean-}
```
public void setSnapToGrid(boolean value)
```


Указывает, должен ли текущий шрифт использовать параметры сетки документа на строку при компоновке.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


Устанавливает интервал (в пунктах) между символами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Интервал (в пунктах) между символами. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean-}
```
public void setStrikeThrough(boolean value)
```


Истинно, если шрифт отформатирован как зачеркнутый текст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


Задает стиль символов, применяемый к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | Стиль символа, примененный к этому форматированию. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


Задает независимый от локали идентификатор стиля символа, примененного к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Независимый от локали идентификатор стиля символа, применяемого к этому форматированию. Значение должно быть одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы. |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Задает имя стиля символов, применяемого к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя стиля символа, примененного к этому форматированию. |

### setSubscript(boolean value) {#setSubscript-boolean-}
```
public void setSubscript(boolean value)
```


Истинно, если шрифт отформатирован как нижний индекс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuperscript(boolean value) {#setSuperscript-boolean-}
```
public void setSuperscript(boolean value)
```


Истинно, если шрифт отформатирован как надстрочный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTextEffect(int value) {#setTextEffect-int-}
```
public void setTextEffect(int value)
```


Устанавливает эффект анимации шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Эффект анимации шрифта. Значение должно быть одним из[TextEffect](../../com.aspose.words/texteffect) константы. |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setThemeColor(int value) {#setThemeColor-int-}
```
public void setThemeColor(int value)
```


Задает цвет темы в применяемой цветовой схеме, связанной с этим объектом Font.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Цвет темы в применяемой цветовой схеме, связанной с этим объектом Font. Значение должно быть одним из[ThemeColor](../../com.aspose.words/themecolor) константы. |

### setThemeFont(int value) {#setThemeFont-int-}
```
public void setThemeFont(int value)
```


Задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Шрифт темы в применяемой схеме шрифтов, связанный с этим объектом Font. Значение должно быть одним из[ThemeFont](../../com.aspose.words/themefont) константы. |

### setThemeFontAscii(int value) {#setThemeFontAscii-int-}
```
public void setThemeFontAscii(int value)
```


Задает шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом Font.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифта, связанной с этим объектом Font. Значение должно быть одним из[ThemeFont](../../com.aspose.words/themefont) константы. |

### setThemeFontBi(int value) {#setThemeFontBi-int-}
```
public void setThemeFontBi(int value)
```


Задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font в документе на языке с письмом справа налево.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Шрифт темы в применяемой схеме шрифтов, связанный с этим объектом Font в документе с письмом справа налево. Значение должно быть одним из[ThemeFont](../../com.aspose.words/themefont) константы. |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int-}
```
public void setThemeFontFarEast(int value)
```


Задает шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font. Значение должно быть одним из[ThemeFont](../../com.aspose.words/themefont) константы. |

### setThemeFontOther(int value) {#setThemeFontOther-int-}
```
public void setThemeFontOther(int value)
```


Задает шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифтов, связанной с этим объектом Font.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифта, связанной с этим объектом Font. Значение должно быть одним из[ThemeFont](../../com.aspose.words/themefont) константы. |

### setTintAndShade(double value) {#setTintAndShade-double-}
```
public void setTintAndShade(double value)
```


Устанавливает двойное значение, которое делает цвет светлее или темнее.

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) нейтрален. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит к исключению java.lang.IllegalArgumentException.

Установка этого свойства для объекта Font с цветами, не относящимися к теме, приводит к исключению java.lang.IllegalStateException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Двойное значение, которое осветляет или затемняет цвет. |

### setUnderline(int value) {#setUnderline-int-}
```
public void setUnderline(int value)
```


Устанавливает тип подчеркивания, применяемого к шрифту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Тип подчеркивания, примененный к шрифту. Значение должно быть одним из[Underline](../../com.aspose.words/underline) константы. |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color-}
```
public void setUnderlineColor(Color value)
```


Устанавливает цвет подчеркивания, применяемого к шрифту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет подчеркивания, примененный к шрифту. |

### solid() {#solid--}
```
public void solid()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

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
