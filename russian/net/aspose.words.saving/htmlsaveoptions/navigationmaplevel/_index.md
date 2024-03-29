---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words для .NET
description: HtmlSaveOptions NavigationMapLevel свойство. Указывает максимальный уровень заголовков заполняемых на навигационной карте при экспорте в форматы EPUB MOBI или AZW3 . Значение по умолчанию3  на С#.
type: docs
weight: 390
url: /ru/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Указывает максимальный уровень заголовков, заполняемых на навигационной карте при экспорте в форматы EPUB, MOBI или AZW3 . Значение по умолчанию:`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Примечания

Карта навигации позволяет пользовательским агентам обеспечивать простой способ навигации по структуре документа. Обычно точки навигации соответствуют заголовкам в документе. Чтобы заполнить заголовки до уровня**Н** присвойте это значение`NavigationMapLevel`.

По умолчанию заполняются три уровня заголовков: абзацы стилей.**Заголовок 1** ,**Заголовок 2** и**Заголовок 3**. Вы можете установить для этого свойства значение от 1 до 9, чтобы запросить соответствующий максимальный уровень. Установка его в ноль приведет к уменьшению карты навигации до корня документа или корней частей документа.

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
