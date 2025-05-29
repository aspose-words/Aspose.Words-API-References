---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words para .NET
description: Mejora tu escritura con el método CheckGrammar de IAiModelText. Mejora fácilmente la precisión de tus documentos con la corrección gramatical avanzada de IA.
type: docs
weight: 10
url: /es/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Comprueba la gramática del documento proporcionado. Esta operación aprovecha el modelo de IA conectado para comprobar la gramática del documento.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sourceDocument | Document | El documento que se está revisando en cuanto a gramática. |
| options | CheckGrammarOptions | Configuraciones opcionales para controlar cómo se revisará la gramática. |

### Valor_devuelto

Un nuevo[`Document`](../../../aspose.words/document/) con gramática revisada.

## Ejemplos

Muestra cómo comprobar la gramática de un documento.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilice modelos de lenguaje generativo OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Ver también

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)
