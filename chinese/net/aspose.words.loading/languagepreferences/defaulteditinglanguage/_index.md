---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: 用于 .NET 的 Aspose.Words
description: LanguagePreferences DefaultEditingLanguage 财产. 获取或设置默认编辑语言 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

获取或设置默认编辑语言。

默认值为EnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## 例子

显示加载文档时如何设置默认语言。

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### 也可以看看

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
