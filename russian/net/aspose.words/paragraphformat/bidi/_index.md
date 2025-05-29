---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat Bidi, позволяющее легко управлять форматированием текста справа налево для повышения читабельности и улучшения макета документа.
type: docs
weight: 50
url: /ru/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Возвращает или задает, является ли этот абзац абзацем с письмом справа налево.

```csharp
public bool Bidi { get; set; }
```

## Примечания

Когда`истинный`, строки и другие встроенные объекты в этом абзаце располагаются справа налево.

## Примеры

Показывает, как определить направление текста в текстовом документе.

```csharp
// Создаем объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите свойство "DocumentDirection" на "DocumentDirection.Auto", чтобы автоматически определить
// направление каждого абзаца текста, который Aspose.Words загружает из открытого текста.
// Свойство «Bidi» каждого абзаца будет хранить его направление.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Определить, что текст на иврите написан справа налево.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Определить английский текст как написанный справа налево.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Показывает, как создавать списки с написанием справа налево, совместимые с языками, с полями BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле BIDIOUTLINE нумерует абзацы, как поля AUTONUM/LISTNUM,
// но виден только при включенном языке редактирования с письмом справа налево, например иврите или арабском.
// В следующем поле будет отображаться «.1», эквивалент RTL номера списка «1.».
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Добавьте еще два поля BIDIOUTLINE, которые будут отображать «.2» и «.3».
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Устанавливаем горизонтальное выравнивание текста для каждого абзаца в документе на RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Если мы включим в Microsoft Word язык редактирования с написанием справа налево, в наших полях будут отображаться числа.
// В противном случае будет отображаться «###».
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
