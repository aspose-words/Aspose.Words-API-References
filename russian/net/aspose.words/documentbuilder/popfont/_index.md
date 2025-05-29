---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentBuilder PopFont, позволяющий легко восстанавливать форматирование символов из стека, улучшая процесс создания документов.
type: docs
weight: 630
url: /ru/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Извлекает форматирование символов, ранее сохраненное в стеке.

```csharp
public void PopFont()
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
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
