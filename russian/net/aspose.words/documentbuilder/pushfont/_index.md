---
title: DocumentBuilder.PushFont
linktitle: PushFont
articleTitle: PushFont
second_title: Aspose.Words для .NET
description: Узнайте, как метод DocumentBuilder PushFont улучшает форматирование документа, сохраняя стили символов для легкого поиска и единообразного дизайна.
type: docs
weight: 640
url: /ru/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Сохраняет текущее форматирование символов в стеке.

```csharp
public void PushFont()
```

## Примеры

Показывает, как использовать стек форматирования конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте форматирование шрифта, затем напишите текст, который будет перед гиперссылкой.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Сохраняем текущую конфигурацию форматирования в стеке.
builder.PushFont();

// Измените текущее форматирование конструктора, применив новый стиль.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", ложь);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Восстанавливаем форматирование шрифта, которое мы сохранили ранее, и удаляем элемент из стека.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Смотрите также

* property [Font](../font/)
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
