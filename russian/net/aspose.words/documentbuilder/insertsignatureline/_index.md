---
title: DocumentBuilder.InsertSignatureLine
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет строку подписи в текущую позицию.
type: docs
weight: 420
url: /ru/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(SignatureLineOptions) {#insertsignatureline}

Вставляет строку подписи в текущую позицию.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Объект, в котором хранятся параметры создания строки подписи. |

### Возвращаемое значение

Только что вставленный узел строки подписи.

### Примеры

Показывает, как подписать документ личным сертификатом и строкой подписи.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Снова открываем наш сохраненный документ и проверяем, что свойства «IsSigned» и «IsValid» равны «true»,
// указание на то, что строка подписи содержит подпись.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertSignatureLine(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) {#insertsignatureline_1}

Вставляет строку подписи в указанную позицию.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Объект, в котором хранятся параметры создания строки подписи. |
| horzPos | RelativeHorizontalPosition | Указывает, где отсчитывается расстояние до линии подписи. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны линии подписи. |
| vertPos | RelativeVerticalPosition | Указывает, где измеряется расстояние до линии подписи. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны линии подписи. |
| wrapType | WrapType | Указывает, как обтекать текст вокруг строки подписи. |

### Возвращаемое значение

Только что вставленный узел строки подписи.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить встроенную строку подписи в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// Строку подписи можно подписать в Microsoft Word, дважды щелкнув по ней.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


