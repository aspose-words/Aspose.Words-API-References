---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words для .NET
description: Hyphenation IsDictionaryRegistered метод. ВозвращаетЛОЖЬ если для указанного языка не зарегистрирован словарь или зарегистрирован пустой словарьистинный иначе на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Возвращает`ЛОЖЬ` если для указанного языка не зарегистрирован словарь или зарегистрирован пустой словарь,`истинный` иначе.

```csharp
public static bool IsDictionaryRegistered(string language)
```

## Примеры

Показывает, как зарегистрировать словарь переносов.

```csharp
// Словарь расстановки переносов содержит список строк, которые определяют правила расстановки переносов для языка словаря.
// Когда документ содержит строки текста, в которых слово можно разделить и продолжить на следующей строке,
// расстановка переносов будет просматривать список строк словаря на наличие подстрок этого слова.
// Если словарь содержит подстроку, то расстановка переносов разделит слово на две строки
// по подстроке и добавляем дефис в первую половину.
// Регистрируем файл словаря из локальной файловой системы в локали "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Открываем документ, содержащий текст с локалью, соответствующей нашему словарю,
// и сохраняем его в формате сохранения с фиксированной страницей. Текст в этом документе будет написан через дефис.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Перезагружаем документ после отмены регистрации словаря,
// и сохраните его в другой PDF-файл, в котором не будет текста с переносами.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Смотрите также

* class [Hyphenation](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
