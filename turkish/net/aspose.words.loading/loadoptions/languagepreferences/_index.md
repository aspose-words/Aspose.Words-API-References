---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words for .NET
description: LoadOptions LanguagePreferences mülk. Belge yüklenirken kullanılacak dil tercihlerini alır C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Belge yüklenirken kullanılacak dil tercihlerini alır.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

## Örnekler

Bir belgeyi yüklerken dil tercihlerinin nasıl uygulanacağını gösterir.

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

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
