---
title: ParagraphFormat.Bidi
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает является ли это абзацем с письмом справа налево.
type: docs
weight: 50
url: /ru/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Получает или задает, является ли это абзацем с письмом справа налево.

```csharp
public bool Bidi { get; set; }
```

### Примечания

Когда`истинный`, прогоны и другие встроенные объекты в этом параграфе располагаются справа налево.

### Примеры

Показывает, как определить направление текста документа в виде открытого текста.

```csharp
// Создаем объект «TxtLoadOptions», который мы можем передать конструктору документа
// чтобы изменить способ загрузки открытого текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите для свойства «DocumentDirection» значение «DocumentDirection.Auto», автоматически обнаруживает
// направление каждого абзаца текста, который Aspose.Words загружает из открытого текста.
// Свойство Bidi каждого абзаца сохранит направление.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Обнаружить текст на иврите как написанный справа налево.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Обнаружение текста на английском языке как справа налево.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Показывает, как создавать совместимые с языками списки с письмом справа налево с полями BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле BIDIOUTLINE нумерует абзацы так же, как поля AUTONUM/LISTNUM,
// но отображается только в том случае, если включен язык редактирования справа налево, например иврит или арабский.
// В следующем поле будет отображаться «.1», RTL-эквивалент номера списка «1.».
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Добавляем еще два поля BIDIOUTLINE, в которых будут отображаться «.2» и «.3».
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Установите горизонтальное выравнивание текста для каждого абзаца документа на RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Если мы включим в Microsoft Word язык редактирования справа налево, в наших полях будут отображаться числа.
// В противном случае они отобразят «###».
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


