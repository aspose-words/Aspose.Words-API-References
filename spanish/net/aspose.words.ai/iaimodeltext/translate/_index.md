---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words para .NET
description: Traduce documentos fácilmente con nuestro método IAiModelText Translate. Aprovecha la IA para obtener traducciones precisas y rápidas en el idioma que desees.
type: docs
weight: 30
url: /es/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Traduce el documento proporcionado al idioma de destino especificado. Esta operación aprovecha el modelo de IA conectado para la traducción de contenido.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sourceDocument | Document | El documento a traducir. |
| targetLanguage | Language | El idioma al que se traducirá el documento. |

### Valor_devuelto

Un nuevo[`Document`](../../../aspose.words/document/)objeto que contiene el documento traducido.

## Ejemplos

Muestra cómo traducir texto utilizando modelos de Google.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilice modelos de lenguaje generativo de Google.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Ver también

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)
