---
title: Class WarningInfoCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.WarningInfoCollection сорт. Представляет типизированную коллекциюWarningInfo объекты.
type: docs
weight: 6640
url: /ru/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Представляет типизированную коллекцию[`WarningInfo`](../warninginfo/) объекты.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Получает элемент по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Удаляет все элементы из коллекции. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов коллекции. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(WarningInfo) | Реализует[`IWarningCallback`](../iwarningcallback/) интерфейс. Добавляет предупреждение в эту коллекцию. |

### Примечания

Вы можете использовать этот объект коллекции как простейшую форму[`IWarningCallback`](../iwarningcallback/) реализация для сбора всех предупреждений, которые Aspose.Words генерирует во время операции загрузки или сохранения. Создайте экземпляр этого класса и присвойте ему [`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) или[`WarningCallback`](../documentbase/warningcallback/) свойство.

### Примеры

Показывает, как настроить свойство для поиска ближайшего соответствия отсутствующему шрифту из доступных источников шрифтов.

```csharp
public void EnableFontSubstitution()
{
    // Откройте документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Назначаем обратный вызов для обработки предупреждений о замене шрифта.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Установить имя шрифта по умолчанию и включить подстановку шрифтов.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // После замены шрифта следует использовать оригинальные метрики шрифта.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Мы получим предупреждение о замене шрифта, если сохраним документ с отсутствующим шрифтом.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Мы также можем проверить предупреждения в коллекции и очистить их.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Вызывается каждый раз, когда во время загрузки/сохранения возникает предупреждение.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Смотрите также

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


