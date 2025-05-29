---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words para .NET
description: Optimice sus documentos con Aspose.Words.AI.CheckGrammarOptions. Descubra las correcciones gramaticales personalizables de IA para una escritura impecable y una mayor claridad.
type: docs
weight: 50
url: /es/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Permite especificar varias opciones mientras se verifica la gramática de un documento usando IA.

```csharp
public class CheckGrammarOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Permite especificar si la IA intentará mejorar la estilística del texto que se está revisando. El valor predeterminado es`FALSO` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Permite especificar si el documento final o revisado se devolverá con el texto corregido. El valor predeterminado es`FALSO` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Permite especificar cualquiera de los dos[`CheckGrammar`](../iaimodeltext/checkgrammar/)intentará preservar el diseño y formato del documento original, o no. El valor predeterminado es`verdadero` . |

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

* espacio de nombres [Aspose.Words.AI](../../aspose.words.ai/)
* asamblea [Aspose.Words](../../)
