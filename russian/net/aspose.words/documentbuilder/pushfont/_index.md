---
title: DocumentBuilder.PushFont
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Сохраняет текущее форматирование символов в стеке.
type: docs
weight: 570
url: /ru/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Сохраняет текущее форматирование символов в стеке.

```csharp
public void PushFont()
```

### Примеры

Показывает, как использовать стек форматирования конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте форматирование шрифта, затем напишите текст перед гиперссылкой.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Сохраняем нашу текущую конфигурацию форматирования в стеке.
builder.PushFont();

// Изменить текущее форматирование построителя, применив новый стиль.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

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
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


