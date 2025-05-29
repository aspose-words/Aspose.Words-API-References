---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase HRef, которое позволяет легко управлять полными адресами гиперссылок для ваших фигур, повышая интерактивность и функциональность вашего дизайна.
type: docs
weight: 250
url: /ru/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Получает или задает полный адрес гиперссылки для фигуры.

```csharp
public string HRef { get; set; }
```

## Примечания

Значение по умолчанию — пустая строка.

Ниже приведены примеры допустимых значений для этого свойства:

Полный URI:`https://www.aspose.com/`.

Полное имя файла:`C:\\Мои документы\\Отчет о продажах.doc`.

Относительный URI:`../../../ресурс.txt`

Относительное имя файла:`..\\Мои документы\\Отчет о продажах.doc`.

Закладка в другом документе:`https://www.aspose.com/Products/Default.aspx#Suites`

Закладка в этом документе:`#BookmakName`.

## Примеры

Показывает, как вставить фигуру, содержащую изображение, а также являющуюся гиперссылкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + щелчок левой кнопкой мыши по фигуре в Microsoft Word откроет новое окно веб-браузера
// и перенаправляем нас к гиперссылке в свойстве "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
