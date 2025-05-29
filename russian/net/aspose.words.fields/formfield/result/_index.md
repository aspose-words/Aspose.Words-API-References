---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FormField Result, легко управляйте и настраивайте строковый вывод полей формы для улучшения пользовательского опыта.
type: docs
weight: 170
url: /ru/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Возвращает или задает строку, представляющую результат этого поля формы.

```csharp
public string Result { get; set; }
```

## Примечания

Для поля текстовой формы результатом является текст, содержащийся в поле.

Для поля формы с флажком результатом может быть «1» или «0», что указывает на то, что флажок установлен или снят.

Для раскрывающегося поля формы результатом является строка, выбранная в раскрывающемся списке.

Параметр`Result` для текстового поля формы не применяется текстовый формат , указанный в[`TextInputFormat`](../textinputformat/) . Если вы хотите задать значение и применить формат , используйте[`SetTextInputValue`](../settextinputvalue/) метод.

Для текстового поля формы[`TextInputDefault`](../textinputdefault/) значение применяется если*value* является`нулевой`.

## Примеры

Показывает, как вставить поле со списком.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Вставьте поле со списком, которое позволит пользователю выбрать вариант из набора строк.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Поле формы будет отображаться в виде HTML-тега «select».
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Смотрите также

* class [FormField](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
