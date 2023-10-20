---
title: BuiltInDocumentProperties.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words для .NET
description: BuiltInDocumentProperties Paragraphs свойство. Представляет оценку количества абзацев в документе на С#.
type: docs
weight: 230
url: /ru/net/aspose.words.properties/builtindocumentproperties/paragraphs/
---
## BuiltInDocumentProperties.Paragraphs property

Представляет оценку количества абзацев в документе.

```csharp
public int Paragraphs { get; set; }
```

## Примечания

Aspose.Words обновляет это свойство при вызове[`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

## Примеры

Показывает, как обновить все метки списков в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words не отслеживает подобные показатели документа в реальном времени.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Чтобы получить точные значения для трех из этих свойств, нам нужно будет обновить их вручную.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Для подсчета строк нам нужно будет вызвать определенную перегрузку метода обновления.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

Показывает, как работать со свойствами документа в категории «Содержимое».

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Используя встроенные свойства,
    // мы можем рассматривать статистику документа, такую как количество слов/страниц/символов, как метаданные, которые можно просмотреть, не открывая документ
    // Доступ к этим свойствам можно получить, щелкнув файл правой кнопкой мыши в проводнике Windows и выбрав «Свойства» > Подробности > Содержание
    // Если мы хотим отобразить эти данные внутри документа, мы можем использовать такие поля, как NUMPAGES, NUMWORDS, NUCHARS и т. д.
    // Кроме того, эти значения можно просмотреть в Microsoft Word, выбрав Файл > Свойства > Дополнительные свойства > Статистика
    // Количество страниц: свойство PageCount показывает количество страниц в реальном времени, и его значение можно присвоить свойству Pages.

     // Свойство «Страницы» хранит количество страниц документа.
    Assert.AreEqual(6, properties.Pages);

    // Встроенные свойства «Слова», «Символы» и «Символы с пробелами» также отображают различную статистику документа,
    // но нам нужно вызвать метод «UpdateWordCount» для всего документа, прежде чем мы сможем ожидать, что они будут содержать точные значения.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Подсчитаем количество строк в документе, а затем присвоим результат встроенному свойству «Строки».
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Назначаем количество узлов «Абзац» в документе встроенному свойству «Абзацы».
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Получите оценку размера файла нашего документа через встроенное свойство «Байт».
    Assert.AreEqual(20310, properties.Bytes);

    // Установите другой шаблон для нашего документа, а затем вручную обновите встроенное свойство «Шаблон», чтобы отразить это изменение.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // «ContentStatus» — описательное встроенное свойство.
    properties.ContentStatus = "Draft";

    // При сохранении встроенное свойство «ContentType» будет содержать тип MIME выходного формата сохранения.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Если документ содержит ссылки и все они актуальны, мы можем установить для свойства «LinksUpToDate» значение «true».
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Подсчитывает строки в документе.
/// Обходит дерево объектов макета документа при построении,
/// подсчет сущностей типа "Строка", которые также содержат реальный текст.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
