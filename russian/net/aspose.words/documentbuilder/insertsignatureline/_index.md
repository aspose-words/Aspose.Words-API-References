---
title: DocumentBuilder.InsertSignatureLine
linktitle: InsertSignatureLine
articleTitle: InsertSignatureLine
second_title: Aspose.Words для .NET
description: Легко добавляйте профессиональные линии подписи в ваши документы с помощью метода DocumentBuilder InsertSignatureLine. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 470
url: /ru/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/)*) {#insertsignatureline}

Вставляет строку подписи в текущую позицию.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Объект, хранящий параметры создания строки подписи. |

### Возвращаемое значение

Узел строки подписи, который был только что вставлен.

## Примеры

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

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

// Повторно откройте наш сохраненный документ и убедитесь, что свойства «IsSigned» и «IsValid» равны «true»,
// указывая, что строка подписи содержит подпись.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertsignatureline_1}

Вставляет строку подписи в указанную позицию.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Объект, хранящий параметры создания строки подписи. |
| horzPos | RelativeHorizontalPosition | Указывает, от какой точки измеряется расстояние до линии подписи. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны строки подписи. |
| vertPos | RelativeVerticalPosition | Указывает, от какой точки измеряется расстояние до линии подписи. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны строки подписи. |
| wrapType | WrapType | Указывает, как обтекать текстом строку подписи. |

### Возвращаемое значение

Узел строки подписи, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить в документ строку встроенной подписи.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
