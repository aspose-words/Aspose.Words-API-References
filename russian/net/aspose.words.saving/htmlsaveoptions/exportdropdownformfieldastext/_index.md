---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ExportDropDownFormFieldAsText свойство. Управляет сохранением полей раскрывающейся формы в формате HTML или MHTML. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Управляет сохранением полей раскрывающейся формы в формате HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Примечания

Если установлено значение`истинный` , экспортирует поля раскрывающейся формы как обычный текст. Когда`ЛОЖЬ`, экспортирует поля раскрывающейся формы как элемент SELECT в HTML.

При экспорте в EPUB текстовые поля формы раскрывающегося списка всегда сохраняются как текст в соответствии с требованиями этого формата .

## Примеры

Показывает, как заставить поля формы раскрывающегося поля со списком сливаться с текстом абзаца при сохранении в HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор документов, чтобы вставить поле со списком с выбранным значением «Два».
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Флаг «ExportDropDownFormFieldAsText» этого объекта SaveOptions позволяет нам
// контролировать, как при сохранении документа в HTML обрабатываются раскрывающиеся списки.
// Установка значения «true» преобразует каждое поле со списком в простой текст
// который отображает текущее выбранное значение поля со списком, фактически замораживая его.
// Установка значения «false» сохранит функциональность поля со списком с помощью <select> и <опция> теги.
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
