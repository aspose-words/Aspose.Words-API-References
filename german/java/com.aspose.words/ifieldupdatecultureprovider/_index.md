---
title: "IFieldUpdateCultureProvider"
linktitle: "IFieldUpdateCultureProvider"
second_title: "Aspose.Words für Java"
description: "Wenn implementiert, liefert er ein CultureInfo‑Objekt, das während der Aktualisierung eines bestimmten Feldes in Java verwendet werden soll."
type: docs
weight: 767
url: /de/java/com.aspose.words/ifieldupdatecultureprovider/
---
```
public interface IFieldUpdateCultureProvider
```

Wenn implementiert, liefert es ein [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo/)‑Objekt, das während der Aktualisierung eines bestimmten Feldes verwendet werden sollte.

 **Examples:** 

Zeigt, wie man eine Kultur angibt, die die Datums‑/Uhrzeitformatierung für jedes Feld analysiert.

```

 public void defineDateTimeFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(FieldType.FIELD_TIME, true);

     doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);

     // Set a provider that returns a culture object specific to each field.
     doc.getFieldOptions().setFieldUpdateCultureProvider(new FieldUpdateCultureProvider());

     FieldTime fieldDate = (FieldTime) doc.getRange().getFields().get(0);
     if (fieldDate.getLocaleId() != EditingLanguage.RUSSIAN)
         fieldDate.setLocaleId(EditingLanguage.RUSSIAN);

     doc.save(getArtifactsDir() + "FieldOptions.UpdateDateTimeFormatting.pdf");
 }

 /// 
 /// Provides a CultureInfo object that should be used during the update of a particular field.
 /// 
 private static class FieldUpdateCultureProvider implements IFieldUpdateCultureProvider {
     /// 
     /// Returns a CultureInfo object to be used during the field's update.
     /// 
     public CultureInfo getCulture(String name, Field field) {
         switch (name) {
             case "ru-RU":
                 CultureInfo culture = new CultureInfo(new Locale(name));
                 DateTimeFormatInfo format = culture.getDateTimeFormat();

                 format.setMonthNames(new String[]{"\u043c\u0435\u0441\u044f\u0446 1", "\u043c\u0435\u0441\u044f\u0446 2", "\u043c\u0435\u0441\u044f\u0446 3", "\u043c\u0435\u0441\u044f\u0446 4", "\u043c\u0435\u0441\u044f\u0446 5", "\u043c\u0435\u0441\u044f\u0446 6", "\u043c\u0435\u0441\u044f\u0446 7", "\u043c\u0435\u0441\u044f\u0446 8", "\u043c\u0435\u0441\u044f\u0446 9", "\u043c\u0435\u0441\u044f\u0446 10", "\u043c\u0435\u0441\u044f\u0446 11", "\u043c\u0435\u0441\u044f\u0446 12", ""});
                 format.setMonthGenitiveNames(format.getMonthNames());
                 format.setAbbreviatedMonthNames(new String[]{"\u043c\u0435\u0441 1", "\u043c\u0435\u0441 2", "\u043c\u0435\u0441 3", "\u043c\u0435\u0441 4", "\u043c\u0435\u0441 5", "\u043c\u0435\u0441 6", "\u043c\u0435\u0441 7", "\u043c\u0435\u0441 8", "\u043c\u0435\u0441 9", "\u043c\u0435\u0441 10", "\u043c\u0435\u0441 11", "\u043c\u0435\u0441 12", ""});
                 format.setAbbreviatedMonthGenitiveNames(format.getAbbreviatedMonthNames());

                 format.setDayNames(new String[]{"\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 7", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 1", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 2", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 3", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 4", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 5", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 6"});
                 format.setAbbreviatedDayNames(new String[]{"\u0434\u0435\u043d\u044c 7", "\u0434\u0435\u043d\u044c 1", "\u0434\u0435\u043d\u044c 2", "\u0434\u0435\u043d\u044c 3", "\u0434\u0435\u043d\u044c 4", "\u0434\u0435\u043d\u044c 5", "\u0434\u0435\u043d\u044c 6"});
                 format.setShortestDayNames(new String[]{"\u04347", "\u04341", "\u04342", "\u04343", "\u04344", "\u04345", "\u04346"});

                 format.setAMDesignator("\u0414\u043e \u043f\u043e\u043b\u0443\u0434\u043d\u044f");
                 format.setPMDesignator("\u041f\u043e\u0441\u043b\u0435 \u043f\u043e\u043b\u0443\u0434\u043d\u044f");

                 final String PATTERN = "yyyy MM (MMMM) dd (dddd) hh:mm:ss tt";
                 format.setLongDatePattern(PATTERN);
                 format.setLongTimePattern(PATTERN);
                 format.setShortDatePattern(PATTERN);
                 format.setShortTimePattern(PATTERN);

                 return culture;
             case "en-US":
                 return new CultureInfo(new Locale(name));
             default:
                 return null;
         }
     }
 }
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCulture(String culture, Field field)](#getCulture-java.lang.String-com.aspose.words.Field) | Gibt ein [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo/)‑Objekt zurück, das während der Aktualisierung des Feldes verwendet wird. |
### getCulture(String culture, Field field) {#getCulture-java.lang.String-com.aspose.words.Field}
```
public abstract System.Globalization.CultureInfo getCulture(String culture, Field field)
```


Gibt ein [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo/)‑Objekt zurück, das während der Aktualisierung des Feldes verwendet wird.

 **Examples:** 

Zeigt, wie man eine Kultur angibt, die die Datums‑/Uhrzeitformatierung für jedes Feld analysiert.

```

 public void defineDateTimeFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(FieldType.FIELD_TIME, true);

     doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);

     // Set a provider that returns a culture object specific to each field.
     doc.getFieldOptions().setFieldUpdateCultureProvider(new FieldUpdateCultureProvider());

     FieldTime fieldDate = (FieldTime) doc.getRange().getFields().get(0);
     if (fieldDate.getLocaleId() != EditingLanguage.RUSSIAN)
         fieldDate.setLocaleId(EditingLanguage.RUSSIAN);

     doc.save(getArtifactsDir() + "FieldOptions.UpdateDateTimeFormatting.pdf");
 }

 /// 
 /// Provides a CultureInfo object that should be used during the update of a particular field.
 /// 
 private static class FieldUpdateCultureProvider implements IFieldUpdateCultureProvider {
     /// 
     /// Returns a CultureInfo object to be used during the field's update.
     /// 
     public CultureInfo getCulture(String name, Field field) {
         switch (name) {
             case "ru-RU":
                 CultureInfo culture = new CultureInfo(new Locale(name));
                 DateTimeFormatInfo format = culture.getDateTimeFormat();

                 format.setMonthNames(new String[]{"\u043c\u0435\u0441\u044f\u0446 1", "\u043c\u0435\u0441\u044f\u0446 2", "\u043c\u0435\u0441\u044f\u0446 3", "\u043c\u0435\u0441\u044f\u0446 4", "\u043c\u0435\u0441\u044f\u0446 5", "\u043c\u0435\u0441\u044f\u0446 6", "\u043c\u0435\u0441\u044f\u0446 7", "\u043c\u0435\u0441\u044f\u0446 8", "\u043c\u0435\u0441\u044f\u0446 9", "\u043c\u0435\u0441\u044f\u0446 10", "\u043c\u0435\u0441\u044f\u0446 11", "\u043c\u0435\u0441\u044f\u0446 12", ""});
                 format.setMonthGenitiveNames(format.getMonthNames());
                 format.setAbbreviatedMonthNames(new String[]{"\u043c\u0435\u0441 1", "\u043c\u0435\u0441 2", "\u043c\u0435\u0441 3", "\u043c\u0435\u0441 4", "\u043c\u0435\u0441 5", "\u043c\u0435\u0441 6", "\u043c\u0435\u0441 7", "\u043c\u0435\u0441 8", "\u043c\u0435\u0441 9", "\u043c\u0435\u0441 10", "\u043c\u0435\u0441 11", "\u043c\u0435\u0441 12", ""});
                 format.setAbbreviatedMonthGenitiveNames(format.getAbbreviatedMonthNames());

                 format.setDayNames(new String[]{"\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 7", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 1", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 2", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 3", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 4", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 5", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 6"});
                 format.setAbbreviatedDayNames(new String[]{"\u0434\u0435\u043d\u044c 7", "\u0434\u0435\u043d\u044c 1", "\u0434\u0435\u043d\u044c 2", "\u0434\u0435\u043d\u044c 3", "\u0434\u0435\u043d\u044c 4", "\u0434\u0435\u043d\u044c 5", "\u0434\u0435\u043d\u044c 6"});
                 format.setShortestDayNames(new String[]{"\u04347", "\u04341", "\u04342", "\u04343", "\u04344", "\u04345", "\u04346"});

                 format.setAMDesignator("\u0414\u043e \u043f\u043e\u043b\u0443\u0434\u043d\u044f");
                 format.setPMDesignator("\u041f\u043e\u0441\u043b\u0435 \u043f\u043e\u043b\u0443\u0434\u043d\u044f");

                 final String PATTERN = "yyyy MM (MMMM) dd (dddd) hh:mm:ss tt";
                 format.setLongDatePattern(PATTERN);
                 format.setLongTimePattern(PATTERN);
                 format.setShortDatePattern(PATTERN);
                 format.setShortTimePattern(PATTERN);

                 return culture;
             case "en-US":
                 return new CultureInfo(new Locale(name));
             default:
                 return null;
         }
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Kultur | java.lang.String | Der Name der für das zu aktualisierende Feld angeforderten Kultur. |
| field | [Field](../../com.aspose.words/field/) | Das Feld, das aktualisiert wird. |

**Returns:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo/) - The culture object that should be used for the field's update.
