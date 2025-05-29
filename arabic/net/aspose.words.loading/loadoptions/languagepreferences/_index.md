---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words لـ .NET
description: اكتشف LoadOptions LanguagePreferences لتخصيص تحميل المستندات باللغات المفضلة، مما يعزز تجربة المستخدم وإمكانية الوصول.
type: docs
weight: 80
url: /ar/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

يحصل على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

## أمثلة

يوضح كيفية تطبيق تفضيلات اللغة عند تحميل مستند.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### أنظر أيضا

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
