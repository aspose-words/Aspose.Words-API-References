---
title: LanguagePreferences.AddEditingLanguage
second_title: Aspose.Words for .NET API Referansı
description: LanguagePreferences yöntem. Ek düzenleme dili ekler.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Ek düzenleme dili ekler.

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

### Örnekler

Belge yüklerken dil tercihlerinin nasıl uygulanacağını gösterir.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Ayrıca bakınız

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* ad alanı [Aspose.Words.Loading](../../languagepreferences/)
* toplantı [Aspose.Words](../../../)


