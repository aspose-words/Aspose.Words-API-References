---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Управляет тем как поля раскрывающихся форм сохраняются в формате HTML или MHTML. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 140
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Управляет тем, как поля раскрывающихся форм сохраняются в формате HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

### Примечания

При установке на`истинный` , экспортирует раскрывающиеся поля формы как обычный текст. Когда`ЛОЖЬ`, экспортирует раскрывающиеся поля формы как элемент SELECT в HTML.

При экспорте в EPUB текстовые поля выпадающей формы всегда сохраняются как текст из-за требований этого формата.

### Примеры

Показывает, как заставить поля формы раскрывающегося списка сливаться с текстом абзаца при сохранении в формате html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор документов, чтобы вставить поле со списком с выбранным значением «Два».
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Флаг "ExportDropDownFormFieldAsText" этого объекта SaveOptions позволяет нам
// управлять тем, как при сохранении документа в HTML обрабатываются раскрывающиеся списки.
// Установка его в "true" преобразует каждое поле со списком в простой текст
// который отображает текущее выбранное значение поля со списком, фактически замораживая его.
// Установка значения "false" сохранит функциональность поля со списком, используя <select> и <опция> теги.
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
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


