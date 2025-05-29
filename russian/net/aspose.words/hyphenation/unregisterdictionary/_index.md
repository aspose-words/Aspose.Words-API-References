---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words для .NET
description: С легкостью удаляйте словари переносов для любого языка с помощью метода UnregisterDictionary, повышая ясность и читабельность текста.
type: docs
weight: 50
url: /ru/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Отменяет регистрацию словаря переносов для указанного языка.

Это отличается от регистрации словаря Null. Отмена регистрации словаря включает обратный вызов для указанного языка.

```csharp
public static void UnregisterDictionary(string language)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | String | Название языка, например "en-US". Подробности см. в документации .NET для "названия культуры" и в RFC 4646. |

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
