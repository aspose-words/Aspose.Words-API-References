---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words для .NET
description: Откройте для себя метод переноса IsDictionaryRegistered, который проверяет, зарегистрирован ли словарь для вашего языка, обеспечивая точную расстановку переносов в ваших приложениях.
type: docs
weight: 30
url: /ru/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Возврат`ЛОЖЬ` если для указанного языка не зарегистрировано ни одного словаря или зарегистрирован нулевой словарь,`истинный` в противном случае.

```csharp
public static bool IsDictionaryRegistered(string language)
```

## Примеры

Показывает, как зарегистрировать словарь переносов.

```csharp
// Словарь переносов содержит список строк, определяющих правила переносов для языка словаря.
// Когда документ содержит строки текста, в которых слово может быть разделено и продолжено на следующей строке,
// расстановка переносов будет просматривать список строк словаря для подстрок этого слова.
// Если словарь содержит подстроку, то перенос разделит слово на две строки
// на подстроку и добавляем дефис к первой половине.
// Регистрируем файл словаря из локальной файловой системы в локали "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Открываем документ, содержащий текст с локалью, соответствующей локали нашего словаря,
// и сохранить его в формате сохранения с фиксированной страницей. Текст в этом документе будет расставлен переносами.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Перезагрузить документ после отмены регистрации словаря,
// и сохраните его в другом PDF-файле, в котором не будет переносов текста.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Смотрите также

* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
