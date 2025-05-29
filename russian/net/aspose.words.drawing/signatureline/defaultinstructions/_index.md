---
title: SignatureLine.DefaultInstructions
linktitle: DefaultInstructions
articleTitle: DefaultInstructions
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SignatureLine DefaultInstructions расширяет возможности диалогового окна «Подпись» с помощью настраиваемых инструкций по умолчанию для удобства пользователя.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/signatureline/defaultinstructions/
---
## SignatureLine.DefaultInstructions property

Возвращает или задает значение, указывающее, что в диалоговом окне «Подписать» отображаются инструкции по умолчанию. Значение по умолчанию для этого свойства:`истинный` .

```csharp
public bool DefaultInstructions { get; set; }
```

## Примеры

Показывает, как создать строку для подписи и вставить ее в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Вставляем фигуру, которая будет содержать строку подписи, внешний вид которой мы
// настраиваем с помощью объекта «SignatureLineOptions», который мы создали выше.
// Если мы вставим фигуру, координаты которой начинаются в правом нижнем углу страницы,
// нам нужно будет указать отрицательные координаты x и y, чтобы сделать фигуру видимой.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Проверяем свойства нашей линии подписи с помощью ее объекта Shape.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Смотрите также

* class [SignatureLine](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
