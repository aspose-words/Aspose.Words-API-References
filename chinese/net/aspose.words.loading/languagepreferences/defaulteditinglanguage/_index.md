---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words for .NET
description: 使用 LanguagePreferences DefaultEditingLanguage 属性管理您的编辑体验。轻松设置和自定义您的默认编辑语言。
type: docs
weight: 20
url: /zh/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

获取或设置默认编辑语言。

默认值为EnglishUS。

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## 例子

显示如何在加载文档时设置默认语言。

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
