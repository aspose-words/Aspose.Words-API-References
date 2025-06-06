---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: .NET için Aspose.Words
description: Düzenleme deneyiminizi LanguagePreferences AddEditingLanguage yöntemiyle geliştirin. Sorunsuz iş akışı için birden fazla düzenleme dilini kolayca ekleyin ve yönetin.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Ek düzenleme dili ekler.

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

## Örnekler

Bir belge yüklenirken dil tercihlerinin nasıl uygulanacağını gösterir.

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
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
