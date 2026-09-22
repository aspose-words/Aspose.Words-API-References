---
title: "Font"
linktitle: "Font"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على سمات الخط مثل اسم الخط وحجم الخط واللون وما إلى ذلك لكائن في Java."
type: docs
weight: 319
url: /ar/java/com.aspose.words/font/
---

**Inheritance:**
java.lang.Object
```
public class Font
```

يحتوي على سمات الخط (اسم الخط، حجم الخط، اللون، وما إلى ذلك) لكائن.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

أنت لا تنشئ مثيلات من الفئة [Font](../../com.aspose.words/font/) مباشرةً. أنت فقط تستخدم [Font](../../com.aspose.words/font/) للوصول إلى خصائص الخط للكائنات المختلفة مثل [Run](../../com.aspose.words/run/)، [Paragraph](../../com.aspose.words/paragraph/)، [Style](../../com.aspose.words/style/)، [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormatting()](#clearFormatting) | يعيد الضبط إلى تنسيق الخط الافتراضي. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAllCaps()](#getAllCaps) | صحيح إذا كان الخط مُنسقًا بأحرف كبيرة بالكامل. |
| [getAutoColor()](#getAutoColor) | يرجع اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في 'auto color'. |
| [getBidi()](#getBidi) | يحدد ما إذا كان محتوى هذا المقطع يجب أن يمتلك خصائص من اليمين إلى اليسار. |
| [getBold()](#getBold) | صحيح إذا كان الخط مُنسقًا كغامق. |
| [getBoldBi()](#getBoldBi) | صحيح إذا كان النص من اليمين إلى اليسار مُنسقًا بالخط العريض. |
| [getBorder()](#getBorder) | يرجع كائن [Border](../../com.aspose.words/border/) الذي يحدد الحد للخط. |
| [getColor()](#getColor) | يحصل على لون الخط. |
| [getComplexScript()](#getComplexScript) | يحدد ما إذا كان محتوى هذا المقطع يجب أن يُعامل كنص مكتوب بخط معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough) | صحيح إذا كان الخط مُنسقًا بنص مشطوب مزدوج. |
| [getEmboss()](#getEmboss) | صحيح إذا تم تنسيق الخط كبارز. |
| [getEmphasisMark()](#getEmphasisMark) | يحصل على علامة التأكيد المطبقة على هذا التنسيق. |
| [getEngrave()](#getEngrave) | صحيح إذا تم تنسيق الخط كمنقوش. |
| [getFill()](#getFill) | يحصل على تنسيق التعبئة للـ [Font](../../com.aspose.words/font/). |
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
| [getHidden()](#getHidden) | صحيح إذا تم تنسيق الخط كنص مخفي. |
| [getHighlightColor()](#getHighlightColor) | يحصل على لون التمييز (العلامة). |
| [getItalic()](#getItalic) | صحيح إذا كان الخط مُنسقًا كخط مائل. |
| [getItalicBi()](#getItalicBi) | صحيح إذا تم تنسيق النص من اليمين إلى اليسار كخط مائل. |
| [getKerning()](#getKerning) | يحصل على حجم الخط الذي يبدأ عنده التباعد بين الحروف. |
| [getLineSpacing()](#getLineSpacing) | يعيد تباعد الأسطر لهذا الخط (بالنقاط). |
| [getLocaleId()](#getLocaleId) | يحصل على معرف اللغة (locale) للأحرف المنسقة. |
| [getLocaleIdBi()](#getLocaleIdBi) | يحصل على معرف اللغة (locale) للأحرف المنسقة من اليمين إلى اليسار. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast) | يحصل على معرف اللغة (locale) للأحرف الآسيوية المنسقة. |
| [getName()](#getName) | يحصل على اسم الخط. |
| [getNameAscii()](#getNameAscii) | يحصل على الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127). |
| [getNameBi()](#getNameBi) | يحصل على اسم الخط في مستند بلغة من اليمين إلى اليسار. |
| [getNameFarEast()](#getNameFarEast) | يحصل على اسم خط شرق آسيوي. |
| [getNameOther()](#getNameOther) | يحصل على الخط المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255. |
| [getNoProofing()](#getNoProofing) | صحيح عندما لا يتم تدقيق إملائي للأحرف المنسقة. |
| [getNumberSpacing()](#getNumberSpacing) | يحصل على نوع التباعد للرقم المعروض. |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOutline()](#getOutline) | صحيح إذا تم تنسيق الخط كخط مخطط. |
| [getPatternType()](#getPatternType) |  |
| [getPosition()](#getPosition) | يحصل على موضع النص (بالنقاط) بالنسبة للخط الأساسي. |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getScaling()](#getScaling) | يحصل على مقياس عرض الأحرف بالنسبة المئوية. |
| [getShading()](#getShading) | يعيد كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل للخط. |
| [getShadow()](#getShadow) | صحيح إذا تم تنسيق الخط كظل. |
| [getSize()](#getSize) | يحصل على حجم الخط بالنقاط. |
| [getSizeBi()](#getSizeBi) | يحصل على حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار. |
| [getSmallCaps()](#getSmallCaps) | صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية. |
| [getSnapToGrid()](#getSnapToGrid) | يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات عدد الأحرف في السطر لشبكة المستند عند التخطيط. |
| [getSpacing()](#getSpacing) | يحصل على المسافة (بالنقاط) بين الأحرف. |
| [getStrikeThrough()](#getStrikeThrough) | صحيح إذا كان الخط مُنسقًا كنص مشطوب. |
| [getStyle()](#getStyle) | يحصل على نمط الأحرف المطبق على هذا التنسيق. |
| [getStyleIdentifier()](#getStyleIdentifier) | يحصل على معرف النمط المستقل عن اللغة لنمط الأحرف المطبق على هذا التنسيق. |
| [getStyleName()](#getStyleName) | يحصل على اسم نمط الأحرف المطبق على هذا التنسيق. |
| [getSubscript()](#getSubscript) | صحيح إذا كان الخط منسقًا كمنخفض. |
| [getSuperscript()](#getSuperscript) | صحيح إذا كان الخط منسقًا كمرتفع. |
| [getTextEffect()](#getTextEffect) | يحصل على تأثير الرسوم المتحركة للخط. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getThemeColor()](#getThemeColor) | يحصل على لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [getThemeFont()](#getThemeFont) | يحصل على خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [getThemeFontAscii()](#getThemeFontAscii) | يحصل على خط السمة المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127) في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [getThemeFontBi()](#getThemeFontBi) | يحصل على خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) في مستند لغة من اليمين إلى اليسار. |
| [getThemeFontFarEast()](#getThemeFontFarEast) | يحصل على خط السمة للشرق الآسيوي في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [getThemeFontOther()](#getThemeFontOther) | يحصل على خط السمة المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255 في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [getTintAndShade()](#getTintAndShade) | يحصل على قيمة مزدوجة تُفتح أو تُغميق اللون. |
| [getUnderline()](#getUnderline) | يحصل على نوع التسطير المطبق على الخط. |
| [getUnderlineColor()](#getUnderlineColor) | يحصل على لون التسطير المطبق على الخط. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean) | صحيح إذا كان الخط مُنسقًا بأحرف كبيرة بالكامل. |
| [setBidi(boolean value)](#setBidi-boolean) | يحدد ما إذا كان محتوى هذا المقطع يجب أن يمتلك خصائص من اليمين إلى اليسار. |
| [setBold(boolean value)](#setBold-boolean) | صحيح إذا كان الخط مُنسقًا كغامق. |
| [setBoldBi(boolean value)](#setBoldBi-boolean) | صحيح إذا كان النص من اليمين إلى اليسار مُنسقًا بالخط العريض. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط لون الخط. |
| [setComplexScript(boolean value)](#setComplexScript-boolean) | يحدد ما إذا كان محتوى هذا المقطع يجب أن يُعامل كنص مكتوب بخط معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean) | صحيح إذا كان الخط مُنسقًا بنص مشطوب مزدوج. |
| [setEmboss(boolean value)](#setEmboss-boolean) | صحيح إذا تم تنسيق الخط كبارز. |
| [setEmphasisMark(int value)](#setEmphasisMark-int) | يضبط علامة التأكيد المطبقة على هذا التنسيق. |
| [setEngrave(boolean value)](#setEngrave-boolean) | صحيح إذا تم تنسيق الخط كمنقوش. |
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
| [setHidden(boolean value)](#setHidden-boolean) | صحيح إذا تم تنسيق الخط كنص مخفي. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color) | يضبط لون التمييز (العلامة). |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setItalic(boolean value)](#setItalic-boolean) | صحيح إذا كان الخط مُنسقًا كخط مائل. |
| [setItalicBi(boolean value)](#setItalicBi-boolean) | صحيح إذا تم تنسيق النص من اليمين إلى اليسار كخط مائل. |
| [setKerning(double value)](#setKerning-double) | يضبط حجم الخط الذي يبدأ عنده التداخل. |
| [setLocaleId(int value)](#setLocaleId-int) | يضبط معرف اللغة (اللغة) للأحرف المنسقة. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int) | يضبط معرف اللغة (اللغة) للأحرف المنسقة من اليمين إلى اليسار. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int) | يضبط معرف اللغة (اللغة) للأحرف الآسيوية المنسقة. |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم الخط. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String) | يضبط الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127). |
| [setNameBi(String value)](#setNameBi-java.lang.String) | يضبط اسم الخط في مستند لغة من اليمين إلى اليسار. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String) | يضبط اسم خط شرق آسيوي. |
| [setNameOther(String value)](#setNameOther-java.lang.String) | يضبط الخط المستخدم للأحرف التي رموزها من 128 إلى 255. |
| [setNoProofing(boolean value)](#setNoProofing-boolean) | صحيح عندما لا يتم تدقيق إملائي للأحرف المنسقة. |
| [setNumberSpacing(int value)](#setNumberSpacing-int) | يضبط نوع التباعد للرقم المعروض. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setOutline(boolean value)](#setOutline-boolean) | صحيح إذا تم تنسيق الخط كخط مخطط. |
| [setPosition(double value)](#setPosition-double) | يضبط موضع النص (بالنقاط) بالنسبة إلى الخط الأساسي. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setScaling(int value)](#setScaling-int) | يضبط مقياس عرض الأحرف بالنسبة المئوية. |
| [setShadow(boolean value)](#setShadow-boolean) | صحيح إذا تم تنسيق الخط كظل. |
| [setSize(double value)](#setSize-double) | يضبط حجم الخط بالنقاط. |
| [setSizeBi(double value)](#setSizeBi-double) | يضبط حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات عدد الأحرف في السطر لشبكة المستند عند التخطيط. |
| [setSpacing(double value)](#setSpacing-double) | يضبط التباعد (بالنقاط) بين الأحرف. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | صحيح إذا كان الخط مُنسقًا كنص مشطوب. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | يضبط نمط الحرف المطبق على هذا التنسيق. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | يضبط معرف النمط المستقل عن اللغة لنمط الحرف المطبق على هذا التنسيق. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | يضبط اسم نمط الحرف المطبق على هذا التنسيق. |
| [setSubscript(boolean value)](#setSubscript-boolean) | صحيح إذا كان الخط منسقًا كمنخفض. |
| [setSuperscript(boolean value)](#setSuperscript-boolean) | صحيح إذا كان الخط منسقًا كمرتفع. |
| [setTextEffect(int value)](#setTextEffect-int) | يضبط تأثير الرسوم المتحركة للخط. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setThemeColor(int value)](#setThemeColor-int) | يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [setThemeFont(int value)](#setThemeFont-int) | يضبط خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int) | يضبط خط السمة المستخدم للنص اللاتيني (الأحرف ذات الرموز من 0 (صفر) إلى 127) في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [setThemeFontBi(int value)](#setThemeFontBi-int) | يضبط خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) في مستند لغة من اليمين إلى اليسار. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int) | يضبط خط السمة شرق آسيوي في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [setThemeFontOther(int value)](#setThemeFontOther-int) | يضبط خط السمة المستخدم للأحرف ذات الرموز من 128 إلى 255 في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). |
| [setTintAndShade(double value)](#setTintAndShade-double) | يضبط قيمة مزدوجة تُفتح أو تُغميق اللون. |
| [setUnderline(int value)](#setUnderline-int) | يضبط نوع الخط السفلي المطبق على الخط. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color) | يضبط لون الخط السفلي المطبق على الخط. |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


يعيد الضبط إلى تنسيق الخط الافتراضي.

 **Remarks:** 

يزيل جميع تنسيقات الخط المحددة صراحةً على الكائن الذي تم الحصول على [Font](../../com.aspose.words/font/) منه، بحيث يتم وراثة تنسيقات الخط من الوالد المناسب.

 **Examples:** 

يوضح كيفية إدراج حقل ارتباط تشعبي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAllCaps() {#getAllCaps}
```
public boolean getAllCaps()
```


صحيح إذا كان الخط مُنسقًا بأحرف كبيرة بالكامل.

 **Examples:** 

يوضح كيفية تنسيق مقطع لعرض محتوياته بأحرف كبيرة.

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
boolean - القيمة المنطقية المقابلة.
### getAutoColor() {#getAutoColor}
```
public Color getAutoColor()
```


يرجع اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في 'اللون التلقائي'. إذا لم يكن اللون 'تلقائي' فسيتم إرجاع [getColor()](../../com.aspose.words/font/#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/font/#setColor-java.awt.Color).

 **Remarks:** 

عندما يكون للنص 'لون تلقائي'، يتم حساب اللون الفعلي للنص تلقائيًا بحيث يكون مقروءًا مقابل لون الخلفية. عند تغيير لون الخلفية، سيتحول لون النص تلقائيًا إلى الأسود أو الأبيض في MS Word لتعزيز الوضوح.

 **Examples:** 

يظهر كيفية تحسين قابلية القراءة عن طريق اختيار لون النص تلقائيًا بناءً على سطوع الخلفية.

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
java.awt.Color - اللون المحسوب الحالي للنص (أسود أو أبيض) المستخدم لـ 'auto color'.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


يحدد ما إذا كان محتوى هذا المقطع يجب أن يمتلك خصائص من اليمين إلى اليسار.

 **Remarks:** 

هذه الخاصية، عندما تكون مفعلة، لا يجب استخدامها مع نص يساري قوي. أي سلوك تحت هذا الشرط غير محدد. هذه الخاصية، عندما تكون معطلة، لا يجب استخدامها مع نص يميني قوي. أي سلوك تحت هذا الشرط غير محدد.

عند عرض محتويات هذا المقطع، يجب معاملة جميع الأحرف كأحرف نصية معقدة لأغراض التنسيق. هذا يعني أن [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean)، [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean)، [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) واسم الخط المقابل سيُستخدم عند عرض هذا المقطع.

أيضًا، عند عرض محتويات هذا المقطع، تعمل هذه الخاصية كإلغاء توجيه من اليمين إلى اليسار للأحرف المصنفة كـ 'أنواع ضعيفة' و'أنواع محايدة'.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
boolean - القيمة المنطقية المقابلة.
### getBold() {#getBold}
```
public boolean getBold()
```


صحيح إذا كان الخط مُنسقًا كغامق.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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
boolean - القيمة المنطقية المقابلة.
### getBoldBi() {#getBoldBi}
```
public boolean getBoldBi()
```


صحيح إذا كان النص من اليمين إلى اليسار مُنسقًا بالخط العريض.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
boolean - القيمة المنطقية المقابلة.
### getBorder() {#getBorder}
```
public Border getBorder()
```


يرجع كائن [Border](../../com.aspose.words/border/) الذي يحدد الحد للخط.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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


يحصل على لون الخط.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية إدراج حقل ارتباط تشعبي.

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
java.awt.Color - لون الخط.
### getComplexScript() {#getComplexScript}
```
public boolean getComplexScript()
```


يحدد ما إذا كان محتوى هذا المقطع يجب أن يُعامل كنص مكتوب بخط معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع.

 **Examples:** 

يظهر كيفية إضافة نص يُعامل دائمًا كنص معقد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDoubleStrikeThrough() {#getDoubleStrikeThrough}
```
public boolean getDoubleStrikeThrough()
```


صحيح إذا كان الخط مُنسقًا بنص مشطوب مزدوج.

 **Examples:** 

يظهر كيفية إضافة خط شطب إلى النص.

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
boolean - القيمة المنطقية المقابلة.
### getEmboss() {#getEmboss}
```
public boolean getEmboss()
```


صحيح إذا تم تنسيق الخط كبارز.

 **Examples:** 

يظهر كيفية تطبيق تأثيرات النقش/البارز على النص.

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
boolean - القيمة المنطقية المقابلة.
### getEmphasisMark() {#getEmphasisMark}
```
public int getEmphasisMark()
```


يحصل على علامة التأكيد المطبقة على هذا التنسيق.

 **Examples:** 

يعرض كيفية إضافة حرف إضافي يُعرض فوق/تحت حرف الشكل.

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
int - علامة التشديد المطبقة على هذا التنسيق. القيمة المرجعة هي واحدة من ثوابت [EmphasisMark](../../com.aspose.words/emphasismark/).
### getEngrave() {#getEngrave}
```
public boolean getEngrave()
```


صحيح إذا تم تنسيق الخط كمنقوش.

 **Examples:** 

يظهر كيفية تطبيق تأثيرات النقش/البارز على النص.

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
boolean - القيمة المنطقية المقابلة.
### getFill() {#getFill}
```
public Fill getFill()
```


يحصل على تنسيق التعبئة للـ [Font](../../com.aspose.words/font/).

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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


صحيح إذا تم تنسيق الخط كنص مخفي.

 **Examples:** 

يظهر كيفية إنشاء مقطع من النص المخفي.

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

يظهر كيفية استخدام تنفيذ DocumentVisitor لإزالة جميع المحتويات المخفية من مستند.

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
boolean - القيمة المنطقية المقابلة.
### getHighlightColor() {#getHighlightColor}
```
public Color getHighlightColor()
```


يحصل على لون التمييز (العلامة).

 **Examples:** 

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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
java.awt.Color - لون التمييز (العلامة).
### getItalic() {#getItalic}
```
public boolean getItalic()
```


صحيح إذا كان الخط مُنسقًا كخط مائل.

 **Examples:** 

يظهر كيفية كتابة نص مائل باستخدام مُنشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getItalicBi() {#getItalicBi}
```
public boolean getItalicBi()
```


صحيح إذا تم تنسيق النص من اليمين إلى اليسار كخط مائل.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
boolean - القيمة المنطقية المقابلة.
### getKerning() {#getKerning}
```
public double getKerning()
```


يحصل على حجم الخط الذي يبدأ عنده التباعد بين الحروف.

 **Examples:** 

يظهر كيفية تحديد حجم الخط الذي يبدأ فيه التباعد بين الحروف (kerning) بالتأثير.

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
double - حجم الخط الذي يبدأ عنده التباعد بين الحروف (kerning).
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


يعيد تباعد الأسطر لهذا الخط (بالنقاط).

 **Examples:** 

يظهر كيفية الحصول على تباعد الأسطر للخط، بالنقاط.

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
double - تباعد الأسطر لهذا الخط (بالنقاط).
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


يحصل على معرف اللغة (locale) للأحرف المنسقة.

 **Remarks:** 

للحصول على قائمة معرفات الإعدادات الإقليمية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

يظهر كيفية تعيين الإعداد الإقليمي للنص الذي نضيفه باستخدام مُنشئ المستند.

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
int - معرف الإعداد الإقليمي (اللغة) للأحرف المُنسقة.
### getLocaleIdBi() {#getLocaleIdBi}
```
public int getLocaleIdBi()
```


يحصل على معرف اللغة (locale) للأحرف المنسقة من اليمين إلى اليسار.

 **Remarks:** 

للحصول على قائمة معرفات الإعدادات الإقليمية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
int - معرف الإعداد الإقليمي (اللغة) للأحرف المُنسقة من اليمين إلى اليسار.
### getLocaleIdFarEast() {#getLocaleIdFarEast}
```
public int getLocaleIdFarEast()
```


يحصل على معرف اللغة (locale) للأحرف الآسيوية المنسقة.

 **Remarks:** 

للحصول على قائمة معرفات الإعدادات الإقليمية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

يظهر كيفية إدراج وتنسيق النص بلغة شرق أقصى.

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
int - معرف الإعداد الإقليمي (اللغة) للأحرف الآسيوية المُنسقة.
### getName() {#getName}
```
public String getName()
```


يحصل على اسم الخط.

 **Remarks:** 

عند الاسترجاع، تُعيد [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

عند الضبط، يضبط [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) و [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) إلى القيمة المحددة.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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
java.lang.String - اسم الخط.
### getNameAscii() {#getNameAscii}
```
public String getNameAscii()
```


يحصل على الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127).

 **Examples:** 

يوضح كيف يمكن لـ Microsoft Word دمج خطين مختلفين في تشغيل واحد.

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
java.lang.String - الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) حتى 127).
### getNameBi() {#getNameBi}
```
public String getNameBi()
```


يحصل على اسم الخط في مستند بلغة من اليمين إلى اليسار.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
java.lang.String - اسم الخط في مستند بلغة من اليمين إلى اليسار.
### getNameFarEast() {#getNameFarEast}
```
public String getNameFarEast()
```


يحصل على اسم خط شرق آسيوي.

 **Examples:** 

يظهر كيفية إدراج وتنسيق النص بلغة شرق أقصى.

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
java.lang.String - اسم خط آسيوي شرقي.
### getNameOther() {#getNameOther}
```
public String getNameOther()
```


يحصل على الخط المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255.

 **Examples:** 

يوضح كيف يمكن لـ Microsoft Word دمج خطين مختلفين في تشغيل واحد.

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
java.lang.String - الخط المستخدم للأحرف ذات رموز الأحرف من 128 حتى 255.
### getNoProofing() {#getNoProofing}
```
public boolean getNoProofing()
```


صحيح عندما لا يتم تدقيق إملائي للأحرف المنسقة.

 **Examples:** 

يوضح كيفية منع تدقيق إملائي للنص بواسطة Microsoft Word.

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
boolean - القيمة المنطقية المقابلة.
### getNumberSpacing() {#getNumberSpacing}
```
public int getNumberSpacing()
```


يحصل على نوع التباعد للرقم المعروض.

 **Examples:** 

يوضح كيفية تعيين نوع تباعد الرقم.

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
int - نوع التباعد للرقم المعروض. القيمة المرجعة هي واحدة من ثوابت [NumSpacing](../../com.aspose.words/numspacing/).
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


صحيح إذا تم تنسيق الخط كخط مخطط.

 **Examples:** 

يوضح كيفية إنشاء تشغيل نص مُنسق كخط خارجي.

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
boolean - القيمة المنطقية المقابلة.
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


يحصل على موضع النص (بالنقاط) بالنسبة إلى الخط الأساسي. الرقم الموجب يرفع النص، والرقم السالب يخفضه.

 **Examples:** 

يوضح كيفية تنسيق النص لإزاحة موضعه.

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
double - موضع النص (بالنقاط) بالنسبة إلى الخط الأساسي.
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


يحصل على مقياس عرض الأحرف بالنسبة المئوية.

 **Examples:** 

يوضح كيفية ضبط التحجيم الأفقي والمسافة بين الأحرف.

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
int - تحجيم عرض الحرف بالنسبة المئوية.
### getShading() {#getShading}
```
public Shading getShading()
```


يعيد كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل للخط.

 **Examples:** 

يوضح كيفية تطبيق تظليل على النص الذي تم إنشاؤه بواسطة مُنشئ المستند.

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


صحيح إذا تم تنسيق الخط كظل.

 **Examples:** 

يوضح كيفية إنشاء تشغيل نص مُنسق بظل.

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
boolean - القيمة المنطقية المقابلة.
### getSize() {#getSize}
```
public double getSize()
```


يحصل على حجم الخط بالنقاط.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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
double - حجم الخط بالنقاط.
### getSizeBi() {#getSizeBi}
```
public double getSizeBi()
```


يحصل على حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
double - حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية.

 **Examples:** 

يوضح كيفية تنسيق مقطع لعرض محتوياته بأحرف كبيرة.

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
boolean - القيمة المنطقية المقابلة.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات عدد الأحرف في السطر لشبكة المستند عند التخطيط.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


يحصل على المسافة (بالنقاط) بين الأحرف.

 **Examples:** 

يوضح كيفية ضبط التحجيم الأفقي والمسافة بين الأحرف.

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
double - التباعد (بالنقاط) بين الأحرف.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


صحيح إذا كان الخط مُنسقًا كنص مشطوب.

 **Examples:** 

يظهر كيفية إضافة خط شطب إلى النص.

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
boolean - القيمة المنطقية المقابلة.
### getStyle() {#getStyle}
```
public Style getStyle()
```


يحصل على نمط الأحرف المطبق على هذا التنسيق.

 **Examples:** 

يطبق خطًا مزدوجًا تحت جميع تشغيلات النص في المستند التي تم تنسيقها بأنماط حرف مخصصة.

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


يحصل على معرف النمط المستقل عن اللغة لنمط الأحرف المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية تغيير نمط النص الموجود.

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
int - معرف النمط المستقل عن الإعدادات الإقليمية لنمط الحرف المطبق على هذا التنسيق. القيمة المرجعة هي واحدة من ثوابت [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


يحصل على اسم نمط الأحرف المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية تغيير نمط النص الموجود.

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
java.lang.String - اسم نمط الحرف المطبق على هذا التنسيق.
### getSubscript() {#getSubscript}
```
public boolean getSubscript()
```


صحيح إذا كان الخط منسقًا كمنخفض.

 **Examples:** 

يوضح كيفية تنسيق النص لإزاحة موضعه.

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
boolean - القيمة المنطقية المقابلة.
### getSuperscript() {#getSuperscript}
```
public boolean getSuperscript()
```


صحيح إذا كان الخط منسقًا كمرتفع.

 **Examples:** 

يوضح كيفية تنسيق النص لإزاحة موضعه.

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
boolean - القيمة المنطقية المقابلة.
### getTextEffect() {#getTextEffect}
```
public int getTextEffect()
```


يحصل على تأثير الرسوم المتحركة للخط.

 **Examples:** 

يعرض كيفية تطبيق تأثير بصري على تشغيل.

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
int - تأثير حركة الخط. القيمة المرجعة هي واحدة من ثوابت [TextEffect](../../com.aspose.words/texteffect/).
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


يحصل على لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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

يظهر كيفية إنشاء واستخدام النمط المموضوع.

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
int - لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). القيمة المرجعة هي واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/).
### getThemeFont() {#getThemeFont}
```
public int getThemeFont()
```


يحصل على خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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

يظهر كيفية إنشاء واستخدام النمط المموضوع.

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
int - خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). القيمة المرجعة هي واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontAscii() {#getThemeFontAscii}
```
public int getThemeFontAscii()
```


يحصل على خط السمة المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127) في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
int - الخط الموضوع المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) حتى 127) في مخطط الخط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) . القيمة المرجعة هي واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/) .
### getThemeFontBi() {#getThemeFontBi}
```
public int getThemeFontBi()
```


يحصل على خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) في مستند لغة من اليمين إلى اليسار.

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
int - الخط الموضوع في مخطط الخط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) في مستند لغة من اليمين إلى اليسار. القيمة المرجعة هي واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/) .
### getThemeFontFarEast() {#getThemeFontFarEast}
```
public int getThemeFontFarEast()
```


يحصل على خط السمة للشرق الآسيوي في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
int - الخط الموضوع للشرق آسيوي في مخطط الخط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) . القيمة المرجعة هي واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/) .
### getThemeFontOther() {#getThemeFontOther}
```
public int getThemeFontOther()
```


يحصل على خط السمة المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255 في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
int - الخط الموضوع المستخدم للأحرف ذات رموز الأحرف من 128 حتى 255 في مخطط الخط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) . القيمة المرجعة هي واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/) .
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


يحصل على قيمة مزدوجة تُفتح أو تُغميق اللون.

**Returns:**
double - قيمة مزدوجة تُفتح أو تُغميق اللون.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


يحصل على نوع التسطير المطبق على الخط.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية إدراج حقل ارتباط تشعبي.

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

يظهر كيفية تكوين نمط ولون خط تحت النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
int - نوع الخط تحت المطبق على الخط. القيمة المرجعة هي واحدة من ثوابت [Underline](../../com.aspose.words/underline/) .
### getUnderlineColor() {#getUnderlineColor}
```
public Color getUnderlineColor()
```


يحصل على لون التسطير المطبق على الخط.

 **Examples:** 

يظهر كيفية تكوين نمط ولون خط تحت النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
java.awt.Color - لون الخط تحت المطبق على الخط.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlEffectType | int |  |

**Returns:**
boolean
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| النمط | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean}
```
public void setAllCaps(boolean value)
```


صحيح إذا كان الخط مُنسقًا بأحرف كبيرة بالكامل.

 **Examples:** 

يوضح كيفية تنسيق مقطع لعرض محتوياته بأحرف كبيرة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


يحدد ما إذا كان محتوى هذا المقطع يجب أن يمتلك خصائص من اليمين إلى اليسار.

 **Remarks:** 

هذه الخاصية، عندما تكون مفعلة، لا يجب استخدامها مع نص يساري قوي. أي سلوك تحت هذا الشرط غير محدد. هذه الخاصية، عندما تكون معطلة، لا يجب استخدامها مع نص يميني قوي. أي سلوك تحت هذا الشرط غير محدد.

عند عرض محتويات هذا المقطع، يجب معاملة جميع الأحرف كأحرف نصية معقدة لأغراض التنسيق. هذا يعني أن [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean)، [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean)، [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) واسم الخط المقابل سيُستخدم عند عرض هذا المقطع.

أيضًا، عند عرض محتويات هذا المقطع، تعمل هذه الخاصية كإلغاء توجيه من اليمين إلى اليسار للأحرف المصنفة كـ 'أنواع ضعيفة' و'أنواع محايدة'.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


صحيح إذا كان الخط مُنسقًا كغامق.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBoldBi(boolean value) {#setBoldBi-boolean}
```
public void setBoldBi(boolean value)
```


صحيح إذا كان النص من اليمين إلى اليسار مُنسقًا بالخط العريض.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط لون الخط.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية إدراج حقل ارتباط تشعبي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون الخط. |

### setComplexScript(boolean value) {#setComplexScript-boolean}
```
public void setComplexScript(boolean value)
```


يحدد ما إذا كان محتوى هذا المقطع يجب أن يُعامل كنص مكتوب بخط معقد بغض النظر عن قيم أحرف Unicode الخاصة به عند تحديد تنسيق هذا المقطع.

 **Examples:** 

يظهر كيفية إضافة نص يُعامل دائمًا كنص معقد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean}
```
public void setDoubleStrikeThrough(boolean value)
```


صحيح إذا كان الخط مُنسقًا بنص مشطوب مزدوج.

 **Examples:** 

يظهر كيفية إضافة خط شطب إلى النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setEmboss(boolean value) {#setEmboss-boolean}
```
public void setEmboss(boolean value)
```


صحيح إذا تم تنسيق الخط كبارز.

 **Examples:** 

يظهر كيفية تطبيق تأثيرات النقش/البارز على النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setEmphasisMark(int value) {#setEmphasisMark-int}
```
public void setEmphasisMark(int value)
```


يضبط علامة التأكيد المطبقة على هذا التنسيق.

 **Examples:** 

يعرض كيفية إضافة حرف إضافي يُعرض فوق/تحت حرف الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | علامة التشديد المطبقة على هذا التنسيق. يجب أن تكون القيمة واحدة من ثوابت [EmphasisMark](../../com.aspose.words/emphasismark/) . |

### setEngrave(boolean value) {#setEngrave-boolean}
```
public void setEngrave(boolean value)
```


صحيح إذا تم تنسيق الخط كمنقوش.

 **Examples:** 

يظهر كيفية تطبيق تأثيرات النقش/البارز على النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


صحيح إذا تم تنسيق الخط كنص مخفي.

 **Examples:** 

يظهر كيفية إنشاء مقطع من النص المخفي.

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

يظهر كيفية استخدام تنفيذ DocumentVisitor لإزالة جميع المحتويات المخفية من مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color}
```
public void setHighlightColor(Color value)
```


يضبط لون التمييز (العلامة).

 **Examples:** 

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون التظليل (العلامة). |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


صحيح إذا كان الخط مُنسقًا كخط مائل.

 **Examples:** 

يظهر كيفية كتابة نص مائل باستخدام مُنشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setItalicBi(boolean value) {#setItalicBi-boolean}
```
public void setItalicBi(boolean value)
```


صحيح إذا تم تنسيق النص من اليمين إلى اليسار كخط مائل.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setKerning(double value) {#setKerning-double}
```
public void setKerning(double value)
```


يضبط حجم الخط الذي يبدأ عنده التداخل.

 **Examples:** 

يظهر كيفية تحديد حجم الخط الذي يبدأ فيه التباعد بين الحروف (kerning) بالتأثير.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | حجم الخط الذي يبدأ عنده التباعد الحرفي (kerning). |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


يضبط معرف اللغة (اللغة) للأحرف المنسقة.

 **Remarks:** 

للحصول على قائمة معرفات الإعدادات الإقليمية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

يظهر كيفية تعيين الإعداد الإقليمي للنص الذي نضيفه باستخدام مُنشئ المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | معرف الإعداد المحلي (اللغة) للأحرف المُنسقة. |

### setLocaleIdBi(int value) {#setLocaleIdBi-int}
```
public void setLocaleIdBi(int value)
```


يضبط معرف اللغة (اللغة) للأحرف المنسقة من اليمين إلى اليسار.

 **Remarks:** 

للحصول على قائمة معرفات الإعدادات الإقليمية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | معرف الإعداد المحلي (اللغة) للأحرف المُنسقة من اليمين إلى اليسار. |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int}
```
public void setLocaleIdFarEast(int value)
```


يضبط معرف اللغة (اللغة) للأحرف الآسيوية المنسقة.

 **Remarks:** 

للحصول على قائمة معرفات الإعدادات الإقليمية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

يظهر كيفية إدراج وتنسيق النص بلغة شرق أقصى.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | معرف الإعداد المحلي (اللغة) للأحرف الآسيوية المُنسقة. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم الخط.

 **Remarks:** 

عند الاسترجاع، تُعيد [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

عند الضبط، يضبط [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) و [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) إلى القيمة المحددة.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم الخط. |

### setNameAscii(String value) {#setNameAscii-java.lang.String}
```
public void setNameAscii(String value)
```


يضبط الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127).

 **Examples:** 

يوضح كيف يمكن لـ Microsoft Word دمج خطين مختلفين في تشغيل واحد.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) حتى 127). |

### setNameBi(String value) {#setNameBi-java.lang.String}
```
public void setNameBi(String value)
```


يضبط اسم الخط في مستند لغة من اليمين إلى اليسار.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم الخط في مستند لغة من اليمين إلى اليسار. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String}
```
public void setNameFarEast(String value)
```


يضبط اسم خط شرق آسيوي.

 **Examples:** 

يظهر كيفية إدراج وتنسيق النص بلغة شرق أقصى.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم خط شرق آسيوي. |

### setNameOther(String value) {#setNameOther-java.lang.String}
```
public void setNameOther(String value)
```


يضبط الخط المستخدم للأحرف التي رموزها من 128 إلى 255.

 **Examples:** 

يوضح كيف يمكن لـ Microsoft Word دمج خطين مختلفين في تشغيل واحد.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | الخط المستخدم للأحرف ذات رموز الأحرف من 128 حتى 255. |

### setNoProofing(boolean value) {#setNoProofing-boolean}
```
public void setNoProofing(boolean value)
```


صحيح عندما لا يتم تدقيق إملائي للأحرف المنسقة.

 **Examples:** 

يوضح كيفية منع تدقيق إملائي للنص بواسطة Microsoft Word.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setNumberSpacing(int value) {#setNumberSpacing-int}
```
public void setNumberSpacing(int value)
```


يضبط نوع التباعد للرقم المعروض.

 **Examples:** 

يوضح كيفية تعيين نوع تباعد الرقم.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نوع التباعد للرقم المعروض. يجب أن تكون القيمة واحدة من ثوابت [NumSpacing](../../com.aspose.words/numspacing/) . |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |

### setOutline(boolean value) {#setOutline-boolean}
```
public void setOutline(boolean value)
```


صحيح إذا تم تنسيق الخط كخط مخطط.

 **Examples:** 

يوضح كيفية إنشاء تشغيل نص مُنسق كخط خارجي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setPosition(double value) {#setPosition-double}
```
public void setPosition(double value)
```


يضبط موضع النص (بالنقاط) بالنسبة للخط الأساسي. الرقم الموجب يرفع النص، والرقم السالب يخفضه.

 **Examples:** 

يوضح كيفية تنسيق النص لإزاحة موضعه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | موضع النص (بالنقاط) بالنسبة للخط الأساسي. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean |  |

### setScaling(int value) {#setScaling-int}
```
public void setScaling(int value)
```


يضبط مقياس عرض الأحرف بالنسبة المئوية.

 **Examples:** 

يوضح كيفية ضبط التحجيم الأفقي والمسافة بين الأحرف.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | توسيع عرض الأحرف بالنسبة المئوية. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


صحيح إذا تم تنسيق الخط كظل.

 **Examples:** 

يوضح كيفية إنشاء تشغيل نص مُنسق بظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


يضبط حجم الخط بالنقاط.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية تنسيق مجموعة نصية باستخدام خاصية الخط الخاصة بها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | حجم الخط بالنقاط. |

### setSizeBi(double value) {#setSizeBi-double}
```
public void setSizeBi(double value)
```


يضبط حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار.

 **Examples:** 

يظهر كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | حجم الخط بالنقاط المستخدم في مستند من اليمين إلى اليسار. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية.

 **Examples:** 

يوضح كيفية تنسيق مقطع لعرض محتوياته بأحرف كبيرة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


يحدد ما إذا كان الخط الحالي يجب أن يستخدم إعدادات عدد الأحرف في السطر لشبكة المستند عند التخطيط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


يضبط التباعد (بالنقاط) بين الأحرف.

 **Examples:** 

يوضح كيفية ضبط التحجيم الأفقي والمسافة بين الأحرف.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | التباعد (بالنقاط) بين الأحرف. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


صحيح إذا كان الخط مُنسقًا كنص مشطوب.

 **Examples:** 

يظهر كيفية إضافة خط شطب إلى النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


يضبط نمط الحرف المطبق على هذا التنسيق.

 **Examples:** 

يطبق خطًا مزدوجًا تحت جميع تشغيلات النص في المستند التي تم تنسيقها بأنماط حرف مخصصة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | نمط الأحرف المطبق على هذا التنسيق. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


يضبط معرف النمط المستقل عن اللغة لنمط الحرف المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية تغيير نمط النص الموجود.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | معرّف النمط المستقل عن اللغة لنمط الأحرف المطبق على هذا التنسيق. يجب أن تكون القيمة واحدة من ثوابت [StyleIdentifier](../../com.aspose.words/styleidentifier/). |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


يضبط اسم نمط الحرف المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية تغيير نمط النص الموجود.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم نمط الأحرف المطبق على هذا التنسيق. |

### setSubscript(boolean value) {#setSubscript-boolean}
```
public void setSubscript(boolean value)
```


صحيح إذا كان الخط منسقًا كمنخفض.

 **Examples:** 

يوضح كيفية تنسيق النص لإزاحة موضعه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSuperscript(boolean value) {#setSuperscript-boolean}
```
public void setSuperscript(boolean value)
```


صحيح إذا كان الخط منسقًا كمرتفع.

 **Examples:** 

يوضح كيفية تنسيق النص لإزاحة موضعه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setTextEffect(int value) {#setTextEffect-int}
```
public void setTextEffect(int value)
```


يضبط تأثير الرسوم المتحركة للخط.

 **Examples:** 

يعرض كيفية تطبيق تأثير بصري على تشغيل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | تأثير الرسوم المتحركة للخط. يجب أن تكون القيمة واحدة من ثوابت [TextEffect](../../com.aspose.words/texteffect/). |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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

يظهر كيفية إنشاء واستخدام النمط المموضوع.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). يجب أن تكون القيمة واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/). |

### setThemeFont(int value) {#setThemeFont-int}
```
public void setThemeFont(int value)
```


يضبط خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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

يظهر كيفية إنشاء واستخدام النمط المموضوع.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). يجب أن تكون القيمة واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontAscii(int value) {#setThemeFontAscii-int}
```
public void setThemeFontAscii(int value)
```


يضبط خط السمة المستخدم للنص اللاتيني (الأحرف ذات الرموز من 0 (صفر) إلى 127) في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | خط السمة المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127) في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). يجب أن تكون القيمة واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontBi(int value) {#setThemeFontBi-int}
```
public void setThemeFontBi(int value)
```


يضبط خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) في مستند لغة من اليمين إلى اليسار.

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | خط السمة في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/) في مستند لغة من اليمين إلى اليسار. يجب أن تكون القيمة واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int}
```
public void setThemeFontFarEast(int value)
```


يضبط خط السمة شرق آسيوي في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | خط السمة للشرق آسيوي في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). يجب أن تكون القيمة واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontOther(int value) {#setThemeFontOther-int}
```
public void setThemeFontOther(int value)
```


يضبط خط السمة المستخدم للأحرف ذات الرموز من 128 إلى 255 في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/).

 **Examples:** 

يظهر كيفية العمل مع خطوط السمة والألوان.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | خط السمة المستخدم للأحرف ذات رموز الأحرف من 128 إلى 255 في مخطط الخطوط المطبق المرتبط بهذا الكائن [Font](../../com.aspose.words/font/). يجب أن تكون القيمة واحدة من ثوابت [ThemeFont](../../com.aspose.words/themefont/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


يضبط قيمة مزدوجة تُفتح أو تُغميق اللون.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تُفتح أو تُغميق اللون. |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


يضبط نوع الخط السفلي المطبق على الخط.

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

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

يوضح كيفية إدراج حقل ارتباط تشعبي.

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

يظهر كيفية تكوين نمط ولون خط تحت النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نوع الخط السفلي المطبق على الخط. يجب أن تكون القيمة واحدة من ثوابت [Underline](../../com.aspose.words/underline/). |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color}
```
public void setUnderlineColor(Color value)
```


يضبط لون الخط السفلي المطبق على الخط.

 **Examples:** 

يظهر كيفية تكوين نمط ولون خط تحت النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون الخط السفلي المطبق على الخط. |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| النمط | int |  |
| variant | int |  |

