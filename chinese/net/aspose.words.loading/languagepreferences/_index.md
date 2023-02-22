---
title: Class LanguagePreferences
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Loading.LanguagePreferences 班级. 允许设置语言首选项
type: docs
weight: 3450
url: /zh/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

允许设置语言首选项。

```csharp
public class LanguagePreferences
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | 获取或设置默认编辑语言。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(EditingLanguage) | 添加额外的编辑语言。 |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(EditingLanguage[]) | 添加其他编辑语言。 |

### 评论

在 Word 中实现“设置 Office 语言首选项”对话框。

### 例子

显示如何在加载文档时应用语言首选项。

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

* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)


