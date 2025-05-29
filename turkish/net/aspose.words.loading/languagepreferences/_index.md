---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: .NET için Aspose.Words
description: Gelişmiş belge işleme için dil ayarlarını zahmetsizce özelleştirmek ve yönetmek amacıyla Aspose.Words.LanguagePreferences sınıfını keşfedin.
type: docs
weight: 4100
url: /tr/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Dil tercihlerini ayarlamanıza olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

```csharp
public class LanguagePreferences
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Varsayılan düzenleme dilini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Ek düzenleme dili ekler. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Ek düzenleme dilleri ekler. |

## Notlar

Word'de 'Office Dil Tercihlerini Ayarla' iletişim kutusunu uygular.

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

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
