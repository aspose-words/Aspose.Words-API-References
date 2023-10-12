---
title: LanguagePreferences.AddEditingLanguage
second_title: Aspose.Words لمراجع .NET API
description: LanguagePreferences طريقة. يضيف لغة تحرير إضافية.
type: docs
weight: 30
url: /ar/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

يضيف لغة تحرير إضافية.

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

### أمثلة

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

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* مساحة الاسم [Aspose.Words.Loading](../../languagepreferences/)
* المجسم [Aspose.Words](../../../)


