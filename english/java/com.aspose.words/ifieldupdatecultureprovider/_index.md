---
title: IFieldUpdateCultureProvider
second_title: Aspose.Words for Java API Reference
description: When implemented provides a  object that should be used during the update of a particular field.
type: docs
weight: 646
url: /java/com.aspose.words/ifieldupdatecultureprovider/
---
```
public interface IFieldUpdateCultureProvider
```

When implemented, provides a [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) object that should be used during the update of a particular field.
## Methods

| Method | Description |
| --- | --- |
| [getCulture(String culture, Field field)](#getCulture-java.lang.String-com.aspose.words.Field) | Returns a [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) object to be used during the field's update. |
### getCulture(String culture, Field field) {#getCulture-java.lang.String-com.aspose.words.Field}
```
public abstract System.Globalization.CultureInfo getCulture(String culture, Field field)
```


Returns a [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) object to be used during the field's update.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| culture | java.lang.String | The name of the culture requested for the field being updated. |
| field | [Field](../../com.aspose.words/field) | The field being updated. |

**Returns:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) - The culture object that should be used for the field's update.
