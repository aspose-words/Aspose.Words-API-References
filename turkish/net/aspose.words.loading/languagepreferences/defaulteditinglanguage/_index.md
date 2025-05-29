---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: .NET için Aspose.Words
description: Düzenleme deneyiminizi LanguagePreferences DefaultEditingLanguage özelliğiyle yönetin. Varsayılan düzenleme dilinizi kolayca ayarlayın ve özelleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Varsayılan düzenleme dilini alır veya ayarlar.

Varsayılan değer:EnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Örnekler

Bir belge yüklenirken varsayılan dilin nasıl ayarlanacağını gösterir.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Ayrıca bakınız

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
