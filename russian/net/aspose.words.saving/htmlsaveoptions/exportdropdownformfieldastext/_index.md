---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ExportDropDownFormFieldAsText улучшает экспорт HTML/MHTML, управляя форматами раскрывающихся полей. Оптимизируйте свои документы!
type: docs
weight: 130
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Управляет сохранением полей раскрывающихся форм в HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Примечания

При установке на`истинный` , экспортирует раскрывающиеся поля формы как обычный текст. Когда`ЛОЖЬ`, экспортирует раскрывающиеся поля формы как элемент SELECT в HTML.

При экспорте в EPUB текстовые поля раскрывающихся форм всегда сохраняются как text due в соответствии с требованиями этого формата.

## Примеры

Показывает, как сделать так, чтобы поля раскрывающегося списка в форме сливались с текстом абзаца при сохранении в HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор документов для вставки поля со списком, в котором выбрано значение «Два».
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Флаг "ExportDropDownFormFieldAsText" этого объекта SaveOptions позволяет нам
// управление тем, как сохранение документа в формате HTML обрабатывает раскрывающиеся списки.
// Установка значения «true» преобразует каждое поле со списком в простой текст
// который отображает текущее выбранное значение поля со списком, фактически замораживая его.
// Установка значения «false» сохранит функциональность поля со списком с использованием тегов <select> и <option>.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
