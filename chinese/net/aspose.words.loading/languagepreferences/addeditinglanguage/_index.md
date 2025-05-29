---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: Aspose.Words for .NET
description: 使用 LanguagePreferences 的 AddEditingLanguage 方法提升您的编辑体验。轻松添加和管理多种编辑语言，实现流畅的工作流程。
type: docs
weight: 30
url: /zh/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

添加额外的编辑语言。

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

## 例子

展示如何在加载文档时应用语言首选项。

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### 也可以看看

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
